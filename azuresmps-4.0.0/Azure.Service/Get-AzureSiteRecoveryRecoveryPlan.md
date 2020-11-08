---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054551"
---
# <span data-ttu-id="6c79b-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c79b-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="6c79b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c79b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c79b-103">Pobiera plan odzyskiwania w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6c79b-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="6c79b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c79b-104">SYNTAX</span></span>

### <span data-ttu-id="6c79b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6c79b-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c79b-106">ById</span><span class="sxs-lookup"><span data-stu-id="6c79b-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c79b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6c79b-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c79b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c79b-108">DESCRIPTION</span></span>
<span data-ttu-id="6c79b-109">Polecenie cmdlet **Get-AzureSiteRecoveryRecoveryPlan** pobiera plan odzyskiwania w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c79b-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="6c79b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c79b-110">EXAMPLES</span></span>

### <span data-ttu-id="6c79b-111">Przykład 1: pobieranie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="6c79b-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="6c79b-112">To polecenie pobiera informacje o planie odzyskiwania bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6c79b-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6c79b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c79b-113">PARAMETERS</span></span>

### <span data-ttu-id="6c79b-114">-ID</span><span class="sxs-lookup"><span data-stu-id="6c79b-114">-Id</span></span>
<span data-ttu-id="6c79b-115">Określa identyfikator planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="6c79b-115">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="6c79b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c79b-116">-Name</span></span>
<span data-ttu-id="6c79b-117">Określa nazwę planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="6c79b-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c79b-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="6c79b-118">-Profile</span></span>
<span data-ttu-id="6c79b-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c79b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c79b-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6c79b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c79b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c79b-121">CommonParameters</span></span>
<span data-ttu-id="6c79b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c79b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c79b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c79b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c79b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c79b-124">INPUTS</span></span>

## <span data-ttu-id="6c79b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c79b-125">OUTPUTS</span></span>

## <span data-ttu-id="6c79b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c79b-126">NOTES</span></span>

## <span data-ttu-id="6c79b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c79b-127">RELATED LINKS</span></span>

[<span data-ttu-id="6c79b-128">Nowe — AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c79b-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6c79b-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c79b-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6c79b-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c79b-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


