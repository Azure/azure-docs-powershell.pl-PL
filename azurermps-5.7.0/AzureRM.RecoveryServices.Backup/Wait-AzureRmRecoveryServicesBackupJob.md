---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526670"
---
# <span data-ttu-id="63f29-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="63f29-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="63f29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63f29-102">SYNOPSIS</span></span>
<span data-ttu-id="63f29-103">Oczekuje na zakończenie zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="63f29-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63f29-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63f29-105">DESCRIPTION</span></span>
<span data-ttu-id="63f29-106">Polecenie cmdlet **wait-AzureRmRecoveryServicesBackupJob** oczekuje na zakończenie zadania kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="63f29-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="63f29-107">Zadania tworzenia kopii zapasowej mogą trwać długo.</span><span class="sxs-lookup"><span data-stu-id="63f29-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="63f29-108">Jeśli uruchomisz zadanie kopii zapasowej w ramach skryptu, możesz wymusić, że skrypt będzie czekał na zakończenie zadania, zanim przełączy się do innych zadań.</span><span class="sxs-lookup"><span data-stu-id="63f29-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="63f29-109">Skrypt zawierający to polecenie cmdlet może być łatwiejszy niż ten, który sonduje usługę kopii zapasowej dla stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="63f29-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="63f29-110">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="63f29-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="63f29-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63f29-111">EXAMPLES</span></span>

### <span data-ttu-id="63f29-112">Przykład 1. oczekiwanie na zakończenie zadania</span><span class="sxs-lookup"><span data-stu-id="63f29-112">Example 1: Wait for a job to finish</span></span>
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

<span data-ttu-id="63f29-113">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="63f29-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="63f29-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63f29-114">PARAMETERS</span></span>

### <span data-ttu-id="63f29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f29-115">-DefaultProfile</span></span>
<span data-ttu-id="63f29-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63f29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f29-117">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="63f29-117">-Job</span></span>
<span data-ttu-id="63f29-118">Określa zadanie oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="63f29-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="63f29-119">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="63f29-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f29-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="63f29-120">-Timeout</span></span>
<span data-ttu-id="63f29-121">Określa maksymalny czas (w sekundach) oczekiwania na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="63f29-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="63f29-122">Zaleca się określenie wartości limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="63f29-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f29-123">CommonParameters</span></span>
<span data-ttu-id="63f29-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f29-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f29-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f29-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63f29-126">INPUTS</span></span>

### <span data-ttu-id="63f29-127">Stream</span><span class="sxs-lookup"><span data-stu-id="63f29-127">Object</span></span>
<span data-ttu-id="63f29-128">Parametr "zadanie" akceptuje wartość typu "Object" z procesu</span><span class="sxs-lookup"><span data-stu-id="63f29-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="63f29-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63f29-129">OUTPUTS</span></span>

### <span data-ttu-id="63f29-130">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="63f29-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="63f29-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. JobBase]</span><span class="sxs-lookup"><span data-stu-id="63f29-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="63f29-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63f29-132">NOTES</span></span>

## <span data-ttu-id="63f29-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63f29-133">RELATED LINKS</span></span>

[<span data-ttu-id="63f29-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="63f29-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


