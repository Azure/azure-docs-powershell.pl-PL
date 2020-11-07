---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892818"
---
# <span data-ttu-id="0e1c7-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e1c7-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0e1c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1c7-103">Ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="0e1c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e1c7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e1c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e1c7-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1c7-106">Polecenie cmdlet **Set-AzApplicationGatewaySslCertificate** ustawia stan celu certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="0e1c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e1c7-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1c7-108">Przykład 1: Ustawianie stanu celu certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="0e1c7-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0e1c7-109">To polecenie ustawia stan celu dla certyfikatu SSL z bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="0e1c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e1c7-110">PARAMETERS</span></span>

### <span data-ttu-id="0e1c7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e1c7-111">-ApplicationGateway</span></span>
<span data-ttu-id="0e1c7-112">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="0e1c7-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="0e1c7-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0e1c7-113">-CertificateFile</span></span>
<span data-ttu-id="0e1c7-114">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="0e1c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1c7-115">-DefaultProfile</span></span>
<span data-ttu-id="0e1c7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e1c7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e1c7-117">-Name</span></span>
<span data-ttu-id="0e1c7-118">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="0e1c7-119">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="0e1c7-119">-Password</span></span>
<span data-ttu-id="0e1c7-120">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="0e1c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1c7-121">CommonParameters</span></span>
<span data-ttu-id="0e1c7-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1c7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1c7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1c7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e1c7-124">INPUTS</span></span>

### <span data-ttu-id="0e1c7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0e1c7-125">System.String</span></span>

## <span data-ttu-id="0e1c7-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e1c7-126">OUTPUTS</span></span>

### <span data-ttu-id="0e1c7-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e1c7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e1c7-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e1c7-128">NOTES</span></span>

## <span data-ttu-id="0e1c7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e1c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="0e1c7-130">Dodaj-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e1c7-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e1c7-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e1c7-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e1c7-132">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e1c7-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e1c7-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e1c7-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


