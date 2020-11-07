---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: ab5697091cf36018601bb2417e42e74f763a5d8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870259"
---
# <span data-ttu-id="09f52-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="09f52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09f52-102">SYNOPSIS</span></span>
<span data-ttu-id="09f52-103">Pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="09f52-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="09f52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09f52-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09f52-105">DESCRIPTION</span></span>
<span data-ttu-id="09f52-106">Polecenie cmdlet **Get-AzApplicationGatewaySslCertificate** pobiera certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="09f52-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="09f52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09f52-107">EXAMPLES</span></span>

### <span data-ttu-id="09f52-108">Przykład 1: uzyskiwanie określonego certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="09f52-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="09f52-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="09f52-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="09f52-110">Drugie polecenie pobiera certyfikat SSL o nazwie Cert01 z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="09f52-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="09f52-111">Polecenie zapisuje certyfikat w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="09f52-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="09f52-112">Przykład 2: uzyskiwanie listy certyfikatów SSL</span><span class="sxs-lookup"><span data-stu-id="09f52-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="09f52-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="09f52-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="09f52-114">W tym drugim poleceniu jest pobierana Lista certyfikatów SSL z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="09f52-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="09f52-115">Polecenie zapisuje wyniki w zmiennej o nazwie $Certs.</span><span class="sxs-lookup"><span data-stu-id="09f52-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="09f52-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09f52-116">PARAMETERS</span></span>

### <span data-ttu-id="09f52-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09f52-117">-ApplicationGateway</span></span>
<span data-ttu-id="09f52-118">Określa obiekt bramy aplikacji, który zawiera certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="09f52-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09f52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f52-119">-DefaultProfile</span></span>
<span data-ttu-id="09f52-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09f52-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f52-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09f52-121">-Name</span></span>
<span data-ttu-id="09f52-122">Określa nazwę puli certyfikatów SSL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f52-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="09f52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f52-123">CommonParameters</span></span>
<span data-ttu-id="09f52-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f52-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09f52-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f52-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f52-126">INPUTS</span></span>

### <span data-ttu-id="09f52-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09f52-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09f52-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09f52-128">OUTPUTS</span></span>

### <span data-ttu-id="09f52-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="09f52-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09f52-130">NOTES</span></span>

## <span data-ttu-id="09f52-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09f52-131">RELATED LINKS</span></span>

[<span data-ttu-id="09f52-132">Dodaj-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09f52-133">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09f52-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="09f52-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09f52-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


