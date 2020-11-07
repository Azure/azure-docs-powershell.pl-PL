---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717874"
---
# <span data-ttu-id="cbeae-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="cbeae-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="cbeae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbeae-102">SYNOPSIS</span></span>
<span data-ttu-id="cbeae-103">Pobiera adres URL jednokrotnego podpisu w profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="cbeae-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbeae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbeae-104">SYNTAX</span></span>

### <span data-ttu-id="cbeae-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cbeae-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbeae-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="cbeae-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbeae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cbeae-107">DESCRIPTION</span></span>
<span data-ttu-id="cbeae-108">Polecenie cmdlet **Get-AzureRmCdnProfileSsoUrl** Pobiera adres URL rejestracji jednokrotnej profilu sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="cbeae-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="cbeae-109">Ten adres URL umożliwia użytkownikom Conntect portalu dodatkowego i korzystanie z dodatkowych funkcji sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="cbeae-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="cbeae-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbeae-110">EXAMPLES</span></span>

## <span data-ttu-id="cbeae-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbeae-111">PARAMETERS</span></span>

### <span data-ttu-id="cbeae-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbeae-112">-CdnProfile</span></span>
<span data-ttu-id="cbeae-113">Określa profil usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="cbeae-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbeae-114">-Refilename</span><span class="sxs-lookup"><span data-stu-id="cbeae-114">-ProfileName</span></span>
<span data-ttu-id="cbeae-115">Określa nazwę profilu usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="cbeae-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbeae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbeae-116">-ResourceGroupName</span></span>
<span data-ttu-id="cbeae-117">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="cbeae-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbeae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbeae-118">-DefaultProfile</span></span>
<span data-ttu-id="cbeae-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbeae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbeae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbeae-120">CommonParameters</span></span>
<span data-ttu-id="cbeae-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbeae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbeae-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbeae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbeae-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbeae-123">INPUTS</span></span>

### <span data-ttu-id="cbeae-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="cbeae-124">PSProfile</span></span>
<span data-ttu-id="cbeae-125">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="cbeae-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="cbeae-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbeae-126">OUTPUTS</span></span>

###  
<span data-ttu-id="cbeae-127">To polecenie cmdlet zwraca adres URL.</span><span class="sxs-lookup"><span data-stu-id="cbeae-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="cbeae-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbeae-128">NOTES</span></span>

## <span data-ttu-id="cbeae-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbeae-129">RELATED LINKS</span></span>

[<span data-ttu-id="cbeae-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cbeae-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


