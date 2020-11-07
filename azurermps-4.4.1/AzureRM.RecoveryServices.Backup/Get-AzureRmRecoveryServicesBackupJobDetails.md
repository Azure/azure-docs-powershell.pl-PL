---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 91658fc0772dfa2752d7f12f93efc62d57330891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717807"
---
# <span data-ttu-id="23956-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="23956-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="23956-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23956-102">SYNOPSIS</span></span>
<span data-ttu-id="23956-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="23956-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23956-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23956-104">SYNTAX</span></span>

### <span data-ttu-id="23956-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23956-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23956-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="23956-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23956-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23956-107">DESCRIPTION</span></span>
<span data-ttu-id="23956-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="23956-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="23956-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="23956-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="23956-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23956-110">EXAMPLES</span></span>

### <span data-ttu-id="23956-111">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="23956-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="23956-112">Pierwsze polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="23956-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="23956-113">Drugie polecenie pobiera szczegóły zadania z nieudanymi zadaniami w $Jobs, a następnie zapisuje je w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="23956-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="23956-114">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="23956-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="23956-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23956-115">PARAMETERS</span></span>

### <span data-ttu-id="23956-116">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="23956-116">-Job</span></span>
<span data-ttu-id="23956-117">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="23956-117">Specifies the job to get.</span></span>
<span data-ttu-id="23956-118">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="23956-118">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="23956-119">-JobId</span><span class="sxs-lookup"><span data-stu-id="23956-119">-JobId</span></span>
<span data-ttu-id="23956-120">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="23956-120">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="23956-121">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="23956-121">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="23956-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23956-122">-DefaultProfile</span></span>
<span data-ttu-id="23956-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23956-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23956-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23956-124">CommonParameters</span></span>
<span data-ttu-id="23956-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23956-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23956-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23956-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23956-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23956-127">INPUTS</span></span>

## <span data-ttu-id="23956-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23956-128">OUTPUTS</span></span>

### <span data-ttu-id="23956-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="23956-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="23956-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23956-130">NOTES</span></span>

## <span data-ttu-id="23956-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23956-131">RELATED LINKS</span></span>

[<span data-ttu-id="23956-132">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="23956-132">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


