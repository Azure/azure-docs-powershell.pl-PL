---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708670"
---
# <span data-ttu-id="4d2f2-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="4d2f2-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="4d2f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2f2-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="4d2f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d2f2-104">SYNTAX</span></span>

### <span data-ttu-id="4d2f2-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d2f2-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d2f2-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="4d2f2-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d2f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d2f2-107">DESCRIPTION</span></span>
<span data-ttu-id="4d2f2-108">Polecenie cmdlet **Get-AzRecoveryServicesBackupJobDetail** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="4d2f2-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4d2f2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d2f2-110">EXAMPLES</span></span>

### <span data-ttu-id="4d2f2-111">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="4d2f2-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="4d2f2-112">Pierwsze polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="4d2f2-113">Drugie polecenie pobiera szczegóły zadania z nieudanymi zadaniami w $Jobs, a następnie zapisuje je w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="4d2f2-114">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="4d2f2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d2f2-115">PARAMETERS</span></span>

### <span data-ttu-id="4d2f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d2f2-116">-DefaultProfile</span></span>
<span data-ttu-id="4d2f2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d2f2-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4d2f2-118">-Job</span></span>
<span data-ttu-id="4d2f2-119">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-119">Specifies the job to get.</span></span>
<span data-ttu-id="4d2f2-120">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d2f2-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="4d2f2-121">-JobId</span></span>
<span data-ttu-id="4d2f2-122">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="4d2f2-123">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="4d2f2-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d2f2-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4d2f2-124">-VaultId</span></span>
<span data-ttu-id="4d2f2-125">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4d2f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2f2-126">CommonParameters</span></span>
<span data-ttu-id="4d2f2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2f2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d2f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2f2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d2f2-129">INPUTS</span></span>

### <span data-ttu-id="4d2f2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4d2f2-130">System.String</span></span>

## <span data-ttu-id="4d2f2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d2f2-131">OUTPUTS</span></span>

### <span data-ttu-id="4d2f2-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4d2f2-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4d2f2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d2f2-133">NOTES</span></span>

## <span data-ttu-id="4d2f2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d2f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d2f2-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4d2f2-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


