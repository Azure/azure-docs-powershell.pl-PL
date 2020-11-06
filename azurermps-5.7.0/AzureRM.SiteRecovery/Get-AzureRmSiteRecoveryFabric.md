---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 63d28696370f5219a4c2a21c6fb3097441a11433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547939"
---
# <span data-ttu-id="8c578-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8c578-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="8c578-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c578-102">SYNOPSIS</span></span>
<span data-ttu-id="8c578-103">Pobierz właściwości sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="8c578-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c578-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c578-104">SYNTAX</span></span>

### <span data-ttu-id="8c578-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8c578-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c578-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8c578-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c578-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8c578-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c578-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c578-108">DESCRIPTION</span></span>
<span data-ttu-id="8c578-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryFabric** pobiera właściwości określonej sieci szkieletowej odzyskiwania witryny platformy Azure lub całej sieci szkieletowej odzyskiwania witryny Azure w magazynie usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8c578-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="8c578-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c578-110">EXAMPLES</span></span>

## <span data-ttu-id="8c578-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c578-111">PARAMETERS</span></span>

### <span data-ttu-id="8c578-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c578-112">-DefaultProfile</span></span>
<span data-ttu-id="8c578-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c578-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c578-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8c578-114">-FriendlyName</span></span>
<span data-ttu-id="8c578-115">Określa przyjazną nazwę sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="8c578-115">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c578-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c578-116">-Name</span></span>
<span data-ttu-id="8c578-117">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="8c578-117">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="8c578-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c578-118">CommonParameters</span></span>
<span data-ttu-id="8c578-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c578-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c578-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c578-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c578-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c578-121">INPUTS</span></span>

### <span data-ttu-id="8c578-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c578-122">None</span></span>
<span data-ttu-id="8c578-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8c578-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c578-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c578-124">OUTPUTS</span></span>

### <span data-ttu-id="8c578-125">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8c578-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8c578-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c578-126">NOTES</span></span>

## <span data-ttu-id="8c578-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c578-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c578-128">Nowe — AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8c578-128">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="8c578-129">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8c578-129">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
