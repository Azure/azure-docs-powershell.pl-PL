---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718736"
---
# <span data-ttu-id="8270d-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8270d-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8270d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8270d-102">SYNOPSIS</span></span>
<span data-ttu-id="8270d-103">Ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8270d-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8270d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8270d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8270d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8270d-105">DESCRIPTION</span></span>
<span data-ttu-id="8270d-106">Polecenie cmdlet **Set-AzureRmApplicationGatewaySslCertificate** ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8270d-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="8270d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8270d-107">EXAMPLES</span></span>

### <span data-ttu-id="8270d-108">Przykład 1: Ustawianie stanu celu certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="8270d-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="8270d-109">To polecenie ustawia stan celu dla certyfikatu SSL z bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="8270d-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="8270d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8270d-110">PARAMETERS</span></span>

### <span data-ttu-id="8270d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8270d-111">-ApplicationGateway</span></span>
<span data-ttu-id="8270d-112">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="8270d-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="8270d-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8270d-113">-CertificateFile</span></span>
<span data-ttu-id="8270d-114">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8270d-114">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8270d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8270d-115">-Name</span></span>
<span data-ttu-id="8270d-116">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8270d-116">Specifies the name of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8270d-117">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="8270d-117">-Password</span></span>
<span data-ttu-id="8270d-118">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8270d-118">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8270d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8270d-119">-DefaultProfile</span></span>
<span data-ttu-id="8270d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8270d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8270d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8270d-121">CommonParameters</span></span>
<span data-ttu-id="8270d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8270d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8270d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8270d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8270d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8270d-124">INPUTS</span></span>

### <span data-ttu-id="8270d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8270d-125">System.String</span></span>

## <span data-ttu-id="8270d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8270d-126">OUTPUTS</span></span>

### <span data-ttu-id="8270d-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8270d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8270d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8270d-128">NOTES</span></span>

## <span data-ttu-id="8270d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8270d-129">RELATED LINKS</span></span>

[<span data-ttu-id="8270d-130">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8270d-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8270d-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8270d-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8270d-132">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8270d-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8270d-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8270d-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


