---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718690"
---
# <span data-ttu-id="3c0c8-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3c0c8-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="3c0c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0c8-103">Pobiera informacje o serwerach odzyskiwania witryny zarejestrowanych w bieżącym magazynie.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c0c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c0c8-104">SYNTAX</span></span>

### <span data-ttu-id="3c0c8-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3c0c8-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c0c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3c0c8-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c0c8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3c0c8-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c0c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3c0c8-108">DESCRIPTION</span></span>
<span data-ttu-id="3c0c8-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryServer** pobiera informacje o serwerach usługi Azure Site Recovery zarejestrowanych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="3c0c8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c0c8-110">EXAMPLES</span></span>

## <span data-ttu-id="3c0c8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c0c8-111">PARAMETERS</span></span>

### <span data-ttu-id="3c0c8-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3c0c8-112">-FriendlyName</span></span>
<span data-ttu-id="3c0c8-113">Określa przyjazną nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-113">Specifies the friendly name of the server.</span></span>

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

### <span data-ttu-id="3c0c8-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c0c8-114">-Name</span></span>
<span data-ttu-id="3c0c8-115">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-115">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3c0c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0c8-116">-DefaultProfile</span></span>
<span data-ttu-id="3c0c8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c0c8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0c8-118">CommonParameters</span></span>
<span data-ttu-id="3c0c8-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0c8-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0c8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0c8-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c0c8-121">INPUTS</span></span>

## <span data-ttu-id="3c0c8-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c0c8-122">OUTPUTS</span></span>

### <span data-ttu-id="3c0c8-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="3c0c8-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="3c0c8-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c0c8-124">NOTES</span></span>

## <span data-ttu-id="3c0c8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c0c8-125">RELATED LINKS</span></span>

[<span data-ttu-id="3c0c8-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="3c0c8-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
