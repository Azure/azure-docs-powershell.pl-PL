---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542899"
---
# <span data-ttu-id="890de-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="890de-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="890de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="890de-102">SYNOPSIS</span></span>
<span data-ttu-id="890de-103">Pobiera witryny Hyper-V z magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="890de-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="890de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="890de-104">SYNTAX</span></span>

### <span data-ttu-id="890de-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="890de-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="890de-106">ByName</span><span class="sxs-lookup"><span data-stu-id="890de-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="890de-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="890de-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="890de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="890de-108">DESCRIPTION</span></span>
<span data-ttu-id="890de-109">Polecenie cmdlet **Get-AzureRmSiteRecoverySite** pobiera witryny Hyper-V w magazynie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="890de-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="890de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="890de-110">EXAMPLES</span></span>

## <span data-ttu-id="890de-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="890de-111">PARAMETERS</span></span>

### <span data-ttu-id="890de-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="890de-112">-FriendlyName</span></span>
<span data-ttu-id="890de-113">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="890de-113">Specifies the friendly name of the site.</span></span>

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

### <span data-ttu-id="890de-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="890de-114">-Name</span></span>
<span data-ttu-id="890de-115">Określa nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="890de-115">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="890de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890de-116">-DefaultProfile</span></span>
<span data-ttu-id="890de-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="890de-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="890de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890de-118">CommonParameters</span></span>
<span data-ttu-id="890de-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890de-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="890de-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890de-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="890de-121">INPUTS</span></span>

## <span data-ttu-id="890de-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="890de-122">OUTPUTS</span></span>

### <span data-ttu-id="890de-123">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="890de-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="890de-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="890de-124">NOTES</span></span>

## <span data-ttu-id="890de-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="890de-125">RELATED LINKS</span></span>

[<span data-ttu-id="890de-126">Nowe — AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="890de-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="890de-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="890de-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
