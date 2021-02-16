---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191834"
---
# <span data-ttu-id="5a087-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a087-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="5a087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a087-102">SYNOPSIS</span></span>
<span data-ttu-id="5a087-103">Tworzy nowy certyfikat główny klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="5a087-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="5a087-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a087-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a087-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a087-105">DESCRIPTION</span></span>
<span data-ttu-id="5a087-106">Polecenie **cmdlet New-AzVpnClientRootCertificate** tworzy nowy certyfikat główny VPN do użycia w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5a087-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="5a087-107">Certyfikaty główne to certyfikaty X.509 identyfikujące główny urząd certyfikacji: wszystkie pozostałe certyfikaty używane w bramie są zaufanymi certyfikatami głównymi.</span><span class="sxs-lookup"><span data-stu-id="5a087-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="5a087-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a087-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="5a087-109">Zamiast tego certyfikat utworzony przez **new-AzVpnClientRootCertificate** jest używany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="5a087-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="5a087-110">Załóżmy na przykład, że tworzysz nowy certyfikat i przechowujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5a087-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="5a087-111">Następnie można użyć tego obiektu certyfikatu podczas tworzenia nowej bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a087-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="5a087-112">Na przykład: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="5a087-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="5a087-113">Aby uzyskać więcej informacji, zapoznaj się z dokumentacją New-AzVirtualNetworkGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a087-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="5a087-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a087-114">EXAMPLES</span></span>

### <span data-ttu-id="5a087-115">Przykład 1. Tworzenie certyfikatu głównego klienta</span><span class="sxs-lookup"><span data-stu-id="5a087-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="5a087-116">W tym przykładzie jest tworzenie certyfikatu głównego klienta i przechowywanie obiektu certyfikatu w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5a087-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="5a087-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a087-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="5a087-118">Pierwsze polecenie używa polecenia cmdlet **Get-Content** w celu uzyskania poprzednio wyeksportowanej tekstowej reprezentacji certyfikatu głównego. że dane tekstowe są przechowywane w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="5a087-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="5a087-119">Drugie polecenie używa pętli w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego i ostatniego wiersza, zapisując wyodrębniony tekst w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="5a087-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="5a087-120">Trzecie polecenie tworzy certyfikat za pomocą polecenia cmdlet **New-AzVpnClientRootCertificate,** przechowując utworzony obiekt w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5a087-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="5a087-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a087-121">PARAMETERS</span></span>

### <span data-ttu-id="5a087-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a087-122">-DefaultProfile</span></span>
<span data-ttu-id="5a087-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a087-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a087-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a087-124">-Name</span></span>
<span data-ttu-id="5a087-125">Określa nazwę nowego certyfikatu głównego klienta.</span><span class="sxs-lookup"><span data-stu-id="5a087-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="5a087-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="5a087-126">-PublicCertData</span></span>
<span data-ttu-id="5a087-127">Określa tekstową reprezentację certyfikatu głównego do dodania.</span><span class="sxs-lookup"><span data-stu-id="5a087-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="5a087-128">Aby uzyskać reprezentację tekstową, wyeksportuj certyfikat w formacie cer (przy użyciu kodowania Base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="5a087-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="5a087-129">Dane wyjściowe powinny być podobne do przedstawionego (należy zauważyć, że rzeczywiste dane wyjściowe będą zawierać o wiele więcej wierszy tekstu niż przedstawiono w przykładzie skróconym): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHGUNEW8343NMJk Certyfikat końcowy -----CVVFAw8w ----- ----- Dane PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (----- BEGIN CERTIFICATE -----) a ostatnim wierszem (----- END CERTIFICATE -----) w pliku.</span><span class="sxs-lookup"><span data-stu-id="5a087-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="5a087-130">Można pobrać dane PublicCertData, używając poleceń programu Windows PowerShell podobnych do tych: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="5a087-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a087-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a087-131">CommonParameters</span></span>
<span data-ttu-id="5a087-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a087-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a087-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a087-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a087-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a087-134">INPUTS</span></span>

### <span data-ttu-id="5a087-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5a087-135">System.String</span></span>

## <span data-ttu-id="5a087-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a087-136">OUTPUTS</span></span>

### <span data-ttu-id="5a087-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a087-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="5a087-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a087-138">NOTES</span></span>

## <span data-ttu-id="5a087-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a087-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a087-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a087-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="5a087-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a087-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="5a087-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a087-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


