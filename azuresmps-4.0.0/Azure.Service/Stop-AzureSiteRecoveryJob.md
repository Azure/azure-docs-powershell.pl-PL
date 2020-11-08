---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055373"
---
# <span data-ttu-id="f8862-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f8862-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="f8862-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8862-102">SYNOPSIS</span></span>
<span data-ttu-id="f8862-103">Zatrzymuje zadanie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="f8862-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="f8862-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8862-104">SYNTAX</span></span>

### <span data-ttu-id="f8862-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8862-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f8862-106">ById</span><span class="sxs-lookup"><span data-stu-id="f8862-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f8862-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8862-107">DESCRIPTION</span></span>
<span data-ttu-id="f8862-108">Polecenie cmdlet **stop-AzureSiteRecoveryJob** zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="f8862-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="f8862-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8862-109">EXAMPLES</span></span>

### <span data-ttu-id="f8862-110">Przykład 1. Zatrzymaj wszystkie zadania</span><span class="sxs-lookup"><span data-stu-id="f8862-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="f8862-111">Pierwsze polecenie pobiera zadania odzyskiwania witryny Azure dla bieżącego magazynu usługi Azure Site Recovery przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** , a następnie zapisuje wyniki w zmiennej $jobs.</span><span class="sxs-lookup"><span data-stu-id="f8862-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="f8862-112">Drugie polecenie zatrzymuje zadania określone przez $Jobs.</span><span class="sxs-lookup"><span data-stu-id="f8862-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="f8862-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8862-113">PARAMETERS</span></span>

### <span data-ttu-id="f8862-114">-ID</span><span class="sxs-lookup"><span data-stu-id="f8862-114">-Id</span></span>
<span data-ttu-id="f8862-115">Określa identyfikator zadania, które ma zostać zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="f8862-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="f8862-116">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="f8862-116">-Job</span></span>
<span data-ttu-id="f8862-117">Określa zadanie, które ma zostać zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="f8862-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="f8862-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="f8862-118">-Profile</span></span>
<span data-ttu-id="f8862-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8862-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f8862-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f8862-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f8862-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8862-121">CommonParameters</span></span>
<span data-ttu-id="f8862-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8862-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8862-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8862-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8862-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8862-124">INPUTS</span></span>

## <span data-ttu-id="f8862-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8862-125">OUTPUTS</span></span>

## <span data-ttu-id="f8862-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8862-126">NOTES</span></span>

## <span data-ttu-id="f8862-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8862-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8862-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f8862-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="f8862-129">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f8862-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="f8862-130">Życiorys — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f8862-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


