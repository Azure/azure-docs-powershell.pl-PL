---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718431"
---
# <span data-ttu-id="ad476-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="ad476-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad476-102">SYNOPSIS</span></span>
<span data-ttu-id="ad476-103">Usuwa plan odzyskiwania witryny z witryny odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="ad476-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad476-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad476-104">SYNTAX</span></span>

### <span data-ttu-id="ad476-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad476-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad476-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ad476-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad476-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad476-107">DESCRIPTION</span></span>
<span data-ttu-id="ad476-108">Polecenie cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** usuwa plan odzyskiwania witryny z bieżącego odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad476-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="ad476-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad476-109">EXAMPLES</span></span>

### <span data-ttu-id="ad476-110">Przykład 1: usuwanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="ad476-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="ad476-111">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmSiteRecoveryRecoveryPlan, aby uzyskać plan odzyskiwania witryny, a następnie przechowywać go w zmiennej $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ad476-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="ad476-112">Drugie polecenie usuwa plan odzyskiwania w $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ad476-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="ad476-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad476-113">PARAMETERS</span></span>

### <span data-ttu-id="ad476-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad476-114">-DefaultProfile</span></span>
<span data-ttu-id="ad476-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad476-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad476-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad476-116">-Name</span></span>
<span data-ttu-id="ad476-117">Określa nazwę planu odzyskiwania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad476-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad476-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-118">-RecoveryPlan</span></span>
<span data-ttu-id="ad476-119">Określa plan odzyskiwania, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad476-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad476-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad476-120">CommonParameters</span></span>
<span data-ttu-id="ad476-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad476-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad476-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad476-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad476-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad476-123">INPUTS</span></span>

### <span data-ttu-id="ad476-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="ad476-125">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ad476-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="ad476-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad476-126">OUTPUTS</span></span>

## <span data-ttu-id="ad476-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad476-127">NOTES</span></span>

## <span data-ttu-id="ad476-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad476-128">RELATED LINKS</span></span>

[<span data-ttu-id="ad476-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ad476-130">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ad476-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad476-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


