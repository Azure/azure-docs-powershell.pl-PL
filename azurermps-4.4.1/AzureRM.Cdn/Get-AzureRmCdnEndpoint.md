---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550080"
---
# <span data-ttu-id="072a9-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="072a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="072a9-102">SYNOPSIS</span></span>
<span data-ttu-id="072a9-103">Pobiera punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="072a9-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="072a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="072a9-104">SYNTAX</span></span>

### <span data-ttu-id="072a9-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="072a9-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="072a9-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="072a9-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="072a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="072a9-107">DESCRIPTION</span></span>
<span data-ttu-id="072a9-108">Polecenie cmdlet **Get-AzureRMCdnEndpoint** umożliwia pobranie punktu końcowego sieci dostarczania zawartości platformy Azure (CDN) i skojarzonych z nim danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="072a9-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="072a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="072a9-109">EXAMPLES</span></span>

## <span data-ttu-id="072a9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="072a9-110">PARAMETERS</span></span>

### <span data-ttu-id="072a9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="072a9-111">-CdnProfile</span></span>
<span data-ttu-id="072a9-112">Określa obiekt profilu sieci CDN, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="072a9-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="072a9-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="072a9-113">-EndpointName</span></span>
<span data-ttu-id="072a9-114">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="072a9-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="072a9-115">Nazwa punktu końcowego nie jest nazwą hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="072a9-115">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072a9-116">-Refilename</span><span class="sxs-lookup"><span data-stu-id="072a9-116">-ProfileName</span></span>
<span data-ttu-id="072a9-117">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="072a9-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="072a9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072a9-118">-ResourceGroupName</span></span>
<span data-ttu-id="072a9-119">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="072a9-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="072a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072a9-120">-DefaultProfile</span></span>
<span data-ttu-id="072a9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="072a9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="072a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072a9-122">CommonParameters</span></span>
<span data-ttu-id="072a9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="072a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072a9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072a9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="072a9-125">INPUTS</span></span>

### <span data-ttu-id="072a9-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="072a9-126">PSProfile</span></span>
<span data-ttu-id="072a9-127">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="072a9-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="072a9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="072a9-128">OUTPUTS</span></span>

###  
<span data-ttu-id="072a9-129">To polecenie cmdlet zwraca obiekt punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="072a9-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="072a9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="072a9-130">NOTES</span></span>

## <span data-ttu-id="072a9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="072a9-131">RELATED LINKS</span></span>

[<span data-ttu-id="072a9-132">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="072a9-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="072a9-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="072a9-135">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="072a9-136">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="072a9-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


