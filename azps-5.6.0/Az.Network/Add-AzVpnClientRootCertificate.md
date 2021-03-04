---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979658"
---
# <span data-ttu-id="78a4f-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="78a4f-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="78a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="78a4f-103">Dodaje certyfikat główny klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="78a4f-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="78a4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78a4f-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78a4f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="78a4f-106">Polecenie **cmdlet Add-AzVpnClientRootCertificate** dodaje certyfikat główny do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="78a4f-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="78a4f-107">Certyfikaty główne to certyfikaty X.509, które identyfikują główny urząd certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="78a4f-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="78a4f-108">Domyślnie wszystkie certyfikaty używane w bramie są zaufane dla certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="78a4f-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="78a4f-109">To polecenie cmdlet przypisuje istniejący certyfikat jako certyfikat główny bramy.</span><span class="sxs-lookup"><span data-stu-id="78a4f-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="78a4f-110">Jeśli certyfikat X.509 nie jest dostępny, można go wygenerować za pośrednictwem infrastruktury kluczy publicznych lub użyć generatora certyfikatów, takiego jak makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="78a4f-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="78a4f-111">Aby dodać certyfikat główny, musisz określić nazwę certyfikatu i podać tylko tekstową reprezentację certyfikatu (aby uzyskać więcej informacji, zobacz parametr *PublicCertData).*</span><span class="sxs-lookup"><span data-stu-id="78a4f-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="78a4f-112">Platforma Azure umożliwia przypisanie więcej niż jednego certyfikatu głównego do bramy.</span><span class="sxs-lookup"><span data-stu-id="78a4f-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="78a4f-113">Wiele certyfikatów głównych jest często wdrażanych przez organizacje, które zawierają użytkowników z więcej niż jednej firmy.</span><span class="sxs-lookup"><span data-stu-id="78a4f-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="78a4f-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78a4f-114">EXAMPLES</span></span>

### <span data-ttu-id="78a4f-115">Przykład 1. Dodawanie certyfikatu głównego klienta do bramy wirtualnej</span><span class="sxs-lookup"><span data-stu-id="78a4f-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="78a4f-116">W tym przykładzie do bramy wirtualnej jest dodano certyfikat główny klienta o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="78a4f-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="78a4f-117">Pierwsze polecenie używa polecenia cmdlet **Get-Content** w celu uzyskania poprzednio wyeksportowanej reprezentacji tekstowej certyfikatu głównego i przechowuje te dane tekstowe zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="78a4f-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="78a4f-118">Drugie polecenie używa pętli w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego i ostatniego wiersza.</span><span class="sxs-lookup"><span data-stu-id="78a4f-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="78a4f-119">Wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="78a4f-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="78a4f-120">Trzecie polecenie użyje następnie tekstu przechowywanego w programie $CertificateText z poleceniem cmdlet **Add-AzVpnClientRootCertificate** w celu dodania certyfikatu głównego do bramy.</span><span class="sxs-lookup"><span data-stu-id="78a4f-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="78a4f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a4f-121">PARAMETERS</span></span>

### <span data-ttu-id="78a4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a4f-122">-DefaultProfile</span></span>
<span data-ttu-id="78a4f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78a4f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a4f-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="78a4f-124">-PublicCertData</span></span>
<span data-ttu-id="78a4f-125">Określa tekstową reprezentację certyfikatu głównego do dodania.</span><span class="sxs-lookup"><span data-stu-id="78a4f-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="78a4f-126">Aby uzyskać reprezentację tekstową, wyeksportuj certyfikat w formacie cer (przy użyciu kodowania Base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="78a4f-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="78a4f-127">W tym przypadku dane wyjściowe będą podobne do poniższych (zwróć uwagę, że rzeczywiste dane wyjściowe będą zawierać o wiele więcej wierszy tekstu niż przedstawiono w przykładzie skróconym): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHGUNEW8343NM Certyfikat KOŃCOWY ----- PublicCertData Jklo09982CVVFAw8w ----- -----. Dane PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (----- BEGIN CERTIFICATE -----) ----- ostatnim wierszem (----- END CERTIFICATE -----) w pliku.</span><span class="sxs-lookup"><span data-stu-id="78a4f-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="78a4f-128">Te dane można pobrać przy użyciu poleceń programu Windows PowerShell podobnych do tych: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="78a4f-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="78a4f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a4f-129">-ResourceGroupName</span></span>
<span data-ttu-id="78a4f-130">Określa nazwę grupy zasobów, do których jest przypisany certyfikat główny.</span><span class="sxs-lookup"><span data-stu-id="78a4f-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="78a4f-131">Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.</span><span class="sxs-lookup"><span data-stu-id="78a4f-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="78a4f-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="78a4f-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="78a4f-133">Określa nazwę bramy sieci wirtualnej, do której został dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="78a4f-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="78a4f-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="78a4f-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="78a4f-135">Określa nazwę certyfikatu głównego klienta, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a4f-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a4f-136">CommonParameters</span></span>
<span data-ttu-id="78a4f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a4f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a4f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a4f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a4f-139">INPUTS</span></span>

### <span data-ttu-id="78a4f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="78a4f-140">System.String</span></span>

## <span data-ttu-id="78a4f-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a4f-141">OUTPUTS</span></span>

### <span data-ttu-id="78a4f-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="78a4f-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="78a4f-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78a4f-143">NOTES</span></span>

## <span data-ttu-id="78a4f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78a4f-144">RELATED LINKS</span></span>

[<span data-ttu-id="78a4f-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="78a4f-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="78a4f-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="78a4f-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="78a4f-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="78a4f-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


