---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547936"
---
# <span data-ttu-id="0dda9-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0dda9-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="0dda9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dda9-102">SYNOPSIS</span></span>
<span data-ttu-id="0dda9-103">Tworzy witrynę odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="0dda9-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dda9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dda9-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dda9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0dda9-105">DESCRIPTION</span></span>
<span data-ttu-id="0dda9-106">Polecenie cmdlet **New-AzureRmSiteRecoverySite** tworzy witrynę Azure Site Recovery w bieżącym magazynie.</span><span class="sxs-lookup"><span data-stu-id="0dda9-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="0dda9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dda9-107">EXAMPLES</span></span>

## <span data-ttu-id="0dda9-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dda9-108">PARAMETERS</span></span>

### <span data-ttu-id="0dda9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dda9-109">-DefaultProfile</span></span>
<span data-ttu-id="0dda9-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dda9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dda9-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0dda9-111">-Name</span></span>
<span data-ttu-id="0dda9-112">Określa nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="0dda9-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dda9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dda9-113">CommonParameters</span></span>
<span data-ttu-id="0dda9-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dda9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dda9-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dda9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dda9-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dda9-116">INPUTS</span></span>

### <span data-ttu-id="0dda9-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0dda9-117">None</span></span>
<span data-ttu-id="0dda9-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0dda9-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0dda9-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dda9-119">OUTPUTS</span></span>

## <span data-ttu-id="0dda9-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dda9-120">NOTES</span></span>

## <span data-ttu-id="0dda9-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dda9-121">RELATED LINKS</span></span>

[<span data-ttu-id="0dda9-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0dda9-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="0dda9-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0dda9-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
