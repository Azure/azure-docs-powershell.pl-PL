---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718446"
---
# <span data-ttu-id="41fb7-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="41fb7-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="41fb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="41fb7-103">Pobiera witryny Hyper-V z magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="41fb7-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41fb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41fb7-104">SYNTAX</span></span>

### <span data-ttu-id="41fb7-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="41fb7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41fb7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="41fb7-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41fb7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="41fb7-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41fb7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="41fb7-109">Polecenie cmdlet **Get-AzureRmSiteRecoverySite** pobiera witryny Hyper-V w magazynie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="41fb7-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="41fb7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41fb7-110">EXAMPLES</span></span>

## <span data-ttu-id="41fb7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41fb7-111">PARAMETERS</span></span>

### <span data-ttu-id="41fb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fb7-112">-DefaultProfile</span></span>
<span data-ttu-id="41fb7-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41fb7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41fb7-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="41fb7-114">-FriendlyName</span></span>
<span data-ttu-id="41fb7-115">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="41fb7-115">Specifies the friendly name of the site.</span></span>

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

### <span data-ttu-id="41fb7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41fb7-116">-Name</span></span>
<span data-ttu-id="41fb7-117">Określa nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="41fb7-117">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="41fb7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fb7-118">CommonParameters</span></span>
<span data-ttu-id="41fb7-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fb7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fb7-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41fb7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fb7-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41fb7-121">INPUTS</span></span>

### <span data-ttu-id="41fb7-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41fb7-122">None</span></span>
<span data-ttu-id="41fb7-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="41fb7-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41fb7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41fb7-124">OUTPUTS</span></span>

### <span data-ttu-id="41fb7-125">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="41fb7-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="41fb7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41fb7-126">NOTES</span></span>

## <span data-ttu-id="41fb7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41fb7-127">RELATED LINKS</span></span>

[<span data-ttu-id="41fb7-128">Nowe — AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="41fb7-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="41fb7-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="41fb7-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
