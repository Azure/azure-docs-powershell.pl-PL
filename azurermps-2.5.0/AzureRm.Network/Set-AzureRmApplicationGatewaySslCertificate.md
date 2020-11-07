---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: bb295ba9f1b7c446e8f8fd6e80d8445774bf8852
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898241"
---
# <span data-ttu-id="8ecfd-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecfd-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8ecfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ecfd-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecfd-103">Ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ecfd-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ecfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ecfd-105">DESCRIPTION</span></span>
<span data-ttu-id="8ecfd-106">Polecenie cmdlet **Set-AzureRmApplicationGatewaySslCertificate** ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="8ecfd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ecfd-107">EXAMPLES</span></span>

### <span data-ttu-id="8ecfd-108">Przykład 1: Ustawianie stanu celu certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="8ecfd-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8ecfd-109">To polecenie ustawia stan celu dla certyfikatu SSL z bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="8ecfd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ecfd-110">PARAMETERS</span></span>

### <span data-ttu-id="8ecfd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ecfd-111">-ApplicationGateway</span></span>
<span data-ttu-id="8ecfd-112">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="8ecfd-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfd-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8ecfd-113">-CertificateFile</span></span>
<span data-ttu-id="8ecfd-114">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="8ecfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecfd-115">-DefaultProfile</span></span>
<span data-ttu-id="8ecfd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ecfd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ecfd-117">-Name</span></span>
<span data-ttu-id="8ecfd-118">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="8ecfd-119">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="8ecfd-119">-Password</span></span>
<span data-ttu-id="8ecfd-120">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecfd-121">CommonParameters</span></span>
<span data-ttu-id="8ecfd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ecfd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecfd-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecfd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecfd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ecfd-124">INPUTS</span></span>

### <span data-ttu-id="8ecfd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecfd-125">System.String</span></span>

## <span data-ttu-id="8ecfd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ecfd-126">OUTPUTS</span></span>

### <span data-ttu-id="8ecfd-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ecfd-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ecfd-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ecfd-128">NOTES</span></span>

## <span data-ttu-id="8ecfd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ecfd-129">RELATED LINKS</span></span>

[<span data-ttu-id="8ecfd-130">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecfd-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8ecfd-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecfd-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8ecfd-132">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecfd-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8ecfd-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecfd-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


