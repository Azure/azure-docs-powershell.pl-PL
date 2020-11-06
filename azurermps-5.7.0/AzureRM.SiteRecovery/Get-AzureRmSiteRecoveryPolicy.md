---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526565"
---
# <span data-ttu-id="3503f-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3503f-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="3503f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3503f-102">SYNOPSIS</span></span>
<span data-ttu-id="3503f-103">Pobiera zasady ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="3503f-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3503f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3503f-104">SYNTAX</span></span>

### <span data-ttu-id="3503f-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3503f-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3503f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3503f-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3503f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3503f-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3503f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3503f-108">DESCRIPTION</span></span>
<span data-ttu-id="3503f-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryPolicy** pobiera listę skonfigurowanych zasad ochrony usługi Azure Site Recovery lub określonych zasad ochrony według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3503f-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="3503f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3503f-110">EXAMPLES</span></span>

## <span data-ttu-id="3503f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3503f-111">PARAMETERS</span></span>

### <span data-ttu-id="3503f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3503f-112">-DefaultProfile</span></span>
<span data-ttu-id="3503f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3503f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3503f-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3503f-114">-FriendlyName</span></span>
<span data-ttu-id="3503f-115">Określa przyjazną nazwę zasad replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="3503f-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="3503f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3503f-116">-Name</span></span>
<span data-ttu-id="3503f-117">Określa nazwę zasad replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="3503f-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="3503f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3503f-118">CommonParameters</span></span>
<span data-ttu-id="3503f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3503f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3503f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3503f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3503f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3503f-121">INPUTS</span></span>

### <span data-ttu-id="3503f-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3503f-122">None</span></span>
<span data-ttu-id="3503f-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3503f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3503f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3503f-124">OUTPUTS</span></span>

### <span data-ttu-id="3503f-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="3503f-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="3503f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3503f-126">NOTES</span></span>

## <span data-ttu-id="3503f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3503f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3503f-128">Nowe — AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3503f-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="3503f-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3503f-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
