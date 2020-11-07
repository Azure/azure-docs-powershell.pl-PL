---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: e32d8312d0046786e6fd36ce30e525241fe78c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706563"
---
# <span data-ttu-id="383e6-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="383e6-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="383e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="383e6-102">SYNOPSIS</span></span>
<span data-ttu-id="383e6-103">Pobiera adres URL jednokrotnego podpisu w profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="383e6-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="383e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="383e6-104">SYNTAX</span></span>

### <span data-ttu-id="383e6-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="383e6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="383e6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="383e6-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="383e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="383e6-107">DESCRIPTION</span></span>
<span data-ttu-id="383e6-108">Polecenie cmdlet **Get-AzCdnProfileSsoUrl** Pobiera adres URL rejestracji jednokrotnej profilu sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="383e6-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="383e6-109">Ten adres URL umożliwia użytkownikom nawiązywanie połączenia z portalem dodatkowym i korzystanie z dodatkowych funkcji sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="383e6-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="383e6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="383e6-110">EXAMPLES</span></span>

## <span data-ttu-id="383e6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="383e6-111">PARAMETERS</span></span>

### <span data-ttu-id="383e6-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="383e6-112">-CdnProfile</span></span>
<span data-ttu-id="383e6-113">Określa profil usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="383e6-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383e6-114">-DefaultProfile</span></span>
<span data-ttu-id="383e6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="383e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383e6-116">-Refilename</span><span class="sxs-lookup"><span data-stu-id="383e6-116">-ProfileName</span></span>
<span data-ttu-id="383e6-117">Określa nazwę profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="383e6-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="383e6-119">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="383e6-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383e6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383e6-120">CommonParameters</span></span>
<span data-ttu-id="383e6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383e6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383e6-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="383e6-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383e6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="383e6-123">INPUTS</span></span>

### <span data-ttu-id="383e6-124">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="383e6-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="383e6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="383e6-125">OUTPUTS</span></span>

### <span data-ttu-id="383e6-126">Microsoft. Azure. Commands. CDN. models. profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="383e6-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="383e6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="383e6-127">NOTES</span></span>

## <span data-ttu-id="383e6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="383e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="383e6-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="383e6-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

