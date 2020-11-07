---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718449"
---
# <span data-ttu-id="998f4-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="998f4-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="998f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="998f4-102">SYNOPSIS</span></span>
<span data-ttu-id="998f4-103">Pobiera informacje o serwerach odzyskiwania witryny zarejestrowanych w bieżącym magazynie.</span><span class="sxs-lookup"><span data-stu-id="998f4-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="998f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="998f4-104">SYNTAX</span></span>

### <span data-ttu-id="998f4-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="998f4-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="998f4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="998f4-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="998f4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="998f4-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="998f4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="998f4-108">DESCRIPTION</span></span>
<span data-ttu-id="998f4-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryServer** pobiera informacje o serwerach usługi Azure Site Recovery zarejestrowanych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="998f4-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="998f4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="998f4-110">EXAMPLES</span></span>

## <span data-ttu-id="998f4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="998f4-111">PARAMETERS</span></span>

### <span data-ttu-id="998f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998f4-112">-DefaultProfile</span></span>
<span data-ttu-id="998f4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="998f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998f4-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="998f4-114">-FriendlyName</span></span>
<span data-ttu-id="998f4-115">Określa przyjazną nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="998f4-115">Specifies the friendly name of the server.</span></span>

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

### <span data-ttu-id="998f4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="998f4-116">-Name</span></span>
<span data-ttu-id="998f4-117">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="998f4-117">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="998f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998f4-118">CommonParameters</span></span>
<span data-ttu-id="998f4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998f4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998f4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998f4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="998f4-121">INPUTS</span></span>

### <span data-ttu-id="998f4-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="998f4-122">None</span></span>
<span data-ttu-id="998f4-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="998f4-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="998f4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="998f4-124">OUTPUTS</span></span>

### <span data-ttu-id="998f4-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="998f4-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="998f4-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="998f4-126">NOTES</span></span>

## <span data-ttu-id="998f4-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="998f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="998f4-128">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="998f4-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
