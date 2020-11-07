---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 9a8f972d9a1107517fa151a714540d4758619913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872564"
---
# <span data-ttu-id="d093b-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d093b-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d093b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d093b-102">SYNOPSIS</span></span>

<span data-ttu-id="d093b-103">Oczekuje na zakończenie zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d093b-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="d093b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d093b-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d093b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d093b-105">DESCRIPTION</span></span>

<span data-ttu-id="d093b-106">Polecenie cmdlet **wait-AzRecoveryServicesBackupJob** oczekuje na zakończenie zadania kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="d093b-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="d093b-107">Zadania tworzenia kopii zapasowej mogą trwać długo.</span><span class="sxs-lookup"><span data-stu-id="d093b-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="d093b-108">Jeśli uruchomisz zadanie kopii zapasowej w ramach skryptu, możesz wymusić, że skrypt będzie czekał na zakończenie zadania, zanim przełączy się do innych zadań.</span><span class="sxs-lookup"><span data-stu-id="d093b-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="d093b-109">Skrypt zawierający to polecenie cmdlet może być łatwiejszy niż ten, który sonduje usługę kopii zapasowej dla stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="d093b-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="d093b-110">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="d093b-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="d093b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d093b-111">EXAMPLES</span></span>

### <span data-ttu-id="d093b-112">Przykład 1. oczekiwanie na zakończenie zadania</span><span class="sxs-lookup"><span data-stu-id="d093b-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="d093b-113">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do czasu ukończenia zadania lub przekroczenia limitu czasu (1 godzina wygasła).</span><span class="sxs-lookup"><span data-stu-id="d093b-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="d093b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d093b-114">PARAMETERS</span></span>

### <span data-ttu-id="d093b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d093b-115">-DefaultProfile</span></span>

<span data-ttu-id="d093b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d093b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d093b-117">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d093b-117">-Job</span></span>

<span data-ttu-id="d093b-118">Określa zadanie oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="d093b-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="d093b-119">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="d093b-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d093b-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="d093b-120">-Timeout</span></span>

<span data-ttu-id="d093b-121">Określa maksymalny czas (w sekundach) oczekiwania na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="d093b-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="d093b-122">Zaleca się określenie wartości limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="d093b-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d093b-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d093b-123">-VaultId</span></span>

<span data-ttu-id="d093b-124">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d093b-124">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d093b-125">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d093b-125">-CommonParameters</span></span>

<span data-ttu-id="d093b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d093b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d093b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d093b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d093b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d093b-128">INPUTS</span></span>

### <span data-ttu-id="d093b-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="d093b-129">System.Object</span></span>

### <span data-ttu-id="d093b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d093b-130">System.String</span></span>

## <span data-ttu-id="d093b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d093b-131">OUTPUTS</span></span>

### <span data-ttu-id="d093b-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d093b-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d093b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d093b-133">NOTES</span></span>

## <span data-ttu-id="d093b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d093b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d093b-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d093b-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
