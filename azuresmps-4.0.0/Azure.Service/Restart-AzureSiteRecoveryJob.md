---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055042"
---
# <span data-ttu-id="e6650-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e6650-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="e6650-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6650-102">SYNOPSIS</span></span>
<span data-ttu-id="e6650-103">Ponowne uruchamianie zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="e6650-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="e6650-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6650-104">SYNTAX</span></span>

### <span data-ttu-id="e6650-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6650-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6650-106">ById</span><span class="sxs-lookup"><span data-stu-id="e6650-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6650-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e6650-107">DESCRIPTION</span></span>
<span data-ttu-id="e6650-108">Polecenie cmdlet **restart-AzureSiteRecoveryJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e6650-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e6650-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6650-109">EXAMPLES</span></span>

### <span data-ttu-id="e6650-110">Przykład 1. Uruchom ponownie zadanie</span><span class="sxs-lookup"><span data-stu-id="e6650-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="e6650-111">To polecenie powoduje ponowne uruchomienie zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="e6650-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="e6650-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6650-112">PARAMETERS</span></span>

### <span data-ttu-id="e6650-113">-ID</span><span class="sxs-lookup"><span data-stu-id="e6650-113">-Id</span></span>
<span data-ttu-id="e6650-114">Określa identyfikator zadania do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e6650-114">Specifies the ID of the job to restart.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6650-115">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="e6650-115">-Job</span></span>
<span data-ttu-id="e6650-116">Określa zadanie ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e6650-116">Specifies the job to restart.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6650-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6650-117">-Profile</span></span>
<span data-ttu-id="e6650-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6650-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6650-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e6650-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6650-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6650-120">CommonParameters</span></span>
<span data-ttu-id="e6650-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6650-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6650-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6650-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6650-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6650-123">INPUTS</span></span>

## <span data-ttu-id="e6650-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6650-124">OUTPUTS</span></span>

## <span data-ttu-id="e6650-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6650-125">NOTES</span></span>

## <span data-ttu-id="e6650-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6650-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6650-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e6650-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e6650-128">Życiorys — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e6650-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e6650-129">Zatrzymaj — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e6650-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


