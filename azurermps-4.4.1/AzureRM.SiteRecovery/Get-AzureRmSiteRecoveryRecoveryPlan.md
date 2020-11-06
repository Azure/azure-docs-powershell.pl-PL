---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542900"
---
# <span data-ttu-id="fbac0-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbac0-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="fbac0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbac0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbac0-103">Pobiera plan odzyskiwania w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="fbac0-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbac0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbac0-104">SYNTAX</span></span>

### <span data-ttu-id="fbac0-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fbac0-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbac0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fbac0-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbac0-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fbac0-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbac0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fbac0-108">DESCRIPTION</span></span>
<span data-ttu-id="fbac0-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryRecoveryPlan** pobiera plan odzyskiwania w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fbac0-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="fbac0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbac0-110">EXAMPLES</span></span>

## <span data-ttu-id="fbac0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbac0-111">PARAMETERS</span></span>

### <span data-ttu-id="fbac0-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fbac0-112">-FriendlyName</span></span>
<span data-ttu-id="fbac0-113">Określa przyjazną nazwę planu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbac0-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbac0-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbac0-114">-Name</span></span>
<span data-ttu-id="fbac0-115">Określa nazwę planu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbac0-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbac0-116">-Path</span><span class="sxs-lookup"><span data-stu-id="fbac0-116">-Path</span></span>
<span data-ttu-id="fbac0-117">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fbac0-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbac0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbac0-118">-DefaultProfile</span></span>
<span data-ttu-id="fbac0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbac0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbac0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbac0-120">CommonParameters</span></span>
<span data-ttu-id="fbac0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbac0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbac0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbac0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbac0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbac0-123">INPUTS</span></span>

## <span data-ttu-id="fbac0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbac0-124">OUTPUTS</span></span>

### <span data-ttu-id="fbac0-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="fbac0-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="fbac0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbac0-126">NOTES</span></span>

## <span data-ttu-id="fbac0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbac0-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbac0-128">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbac0-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fbac0-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbac0-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fbac0-130">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbac0-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
