---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548607"
---
# <span data-ttu-id="4d532-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4d532-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="4d532-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d532-102">SYNOPSIS</span></span>
<span data-ttu-id="4d532-103">Oczekuje na zakończenie zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4d532-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d532-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d532-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d532-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d532-105">DESCRIPTION</span></span>
<span data-ttu-id="4d532-106">Polecenie cmdlet **wait-AzureRmRecoveryServicesBackupJob** oczekuje na zakończenie zadania kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="4d532-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="4d532-107">Zadania tworzenia kopii zapasowej mogą trwać długo.</span><span class="sxs-lookup"><span data-stu-id="4d532-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="4d532-108">Jeśli uruchomisz zadanie kopii zapasowej w ramach skryptu, możesz wymusić, że skrypt będzie czekał na zakończenie zadania, zanim przełączy się do innych zadań.</span><span class="sxs-lookup"><span data-stu-id="4d532-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="4d532-109">Skrypt zawierający to polecenie cmdlet może być łatwiejszy niż ten, który sonduje usługę kopii zapasowej dla stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="4d532-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="4d532-110">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="4d532-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4d532-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d532-111">EXAMPLES</span></span>

### <span data-ttu-id="4d532-112">Przykład 1. oczekiwanie na zakończenie zadania</span><span class="sxs-lookup"><span data-stu-id="4d532-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="4d532-113">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="4d532-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="4d532-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d532-114">PARAMETERS</span></span>

### <span data-ttu-id="4d532-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d532-115">-DefaultProfile</span></span>
<span data-ttu-id="4d532-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d532-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d532-117">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4d532-117">-Job</span></span>
<span data-ttu-id="4d532-118">Określa zadanie oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="4d532-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="4d532-119">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="4d532-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="4d532-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="4d532-120">-Timeout</span></span>
<span data-ttu-id="4d532-121">Określa maksymalny czas (w sekundach) oczekiwania na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="4d532-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="4d532-122">Zaleca się określenie wartości limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="4d532-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="4d532-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4d532-123">-VaultId</span></span>
<span data-ttu-id="4d532-124">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4d532-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4d532-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d532-125">CommonParameters</span></span>
<span data-ttu-id="4d532-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d532-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d532-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d532-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d532-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d532-128">INPUTS</span></span>

### <span data-ttu-id="4d532-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d532-129">System.Object</span></span>
<span data-ttu-id="4d532-130">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d532-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="4d532-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d532-131">System.String</span></span>
<span data-ttu-id="4d532-132">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d532-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="4d532-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d532-133">OUTPUTS</span></span>

### <span data-ttu-id="4d532-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4d532-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4d532-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d532-135">NOTES</span></span>

## <span data-ttu-id="4d532-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d532-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d532-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4d532-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


