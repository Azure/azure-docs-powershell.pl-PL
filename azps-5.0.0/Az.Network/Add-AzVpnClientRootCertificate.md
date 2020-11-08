---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234482"
---
# <span data-ttu-id="56c9b-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56c9b-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="56c9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="56c9b-103">Dodaje certyfikat główny klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="56c9b-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="56c9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56c9b-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56c9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="56c9b-106">Polecenie cmdlet **Add-AzVpnClientRootCertificate** dodaje certyfikat główny do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56c9b-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="56c9b-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="56c9b-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="56c9b-108">Według projektu wszystkie certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="56c9b-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="56c9b-109">To polecenie cmdlet przypisuje istniejący certyfikat jako certyfikat główny bramy.</span><span class="sxs-lookup"><span data-stu-id="56c9b-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="56c9b-110">Jeśli nie masz dostępnego certyfikatu X. 509, możesz wygenerować go za pośrednictwem infrastruktury klucza publicznego lub użyć generatora certyfikatów, takiego jak makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="56c9b-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="56c9b-111">Aby dodać certyfikat główny, należy określić nazwę certyfikatu i przekazać reprezentację tylko tekstową certyfikatu (Aby uzyskać więcej informacji, zobacz parametr *PublicCertData* ).</span><span class="sxs-lookup"><span data-stu-id="56c9b-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="56c9b-112">Azure umożliwia przypisywanie więcej niż jednego certyfikatu głównego do bramy.</span><span class="sxs-lookup"><span data-stu-id="56c9b-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="56c9b-113">Wiele certyfikatów głównych jest często wdrażanych przez organizacje, które zawierają użytkowników z więcej niż jednej firmy.</span><span class="sxs-lookup"><span data-stu-id="56c9b-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="56c9b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56c9b-114">EXAMPLES</span></span>

### <span data-ttu-id="56c9b-115">Przykład 1: Dodawanie głównego certyfikatu klienta do bramy wirtualnej</span><span class="sxs-lookup"><span data-stu-id="56c9b-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="56c9b-116">W tym przykładzie jest dodawany certyfikat główny klienta do bramy wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="56c9b-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="56c9b-117">W pierwszym poleceniu jest używane polecenie **Get-Content** , które pozwala uzyskać uprzednio wyeksportowaną reprezentację głównego certyfikatu głównego i przechowywać w nim dane tekstowe o zmiennej nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="56c9b-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="56c9b-118">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza.</span><span class="sxs-lookup"><span data-stu-id="56c9b-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="56c9b-119">Wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="56c9b-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="56c9b-120">Trzecia komenda korzysta z tekstu przechowywanego w $CertificateText za pomocą polecenia cmdlet **Add-AzVpnClientRootCertificate** w celu dodania głównego certyfikatu do bramy.</span><span class="sxs-lookup"><span data-stu-id="56c9b-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="56c9b-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56c9b-121">PARAMETERS</span></span>

### <span data-ttu-id="56c9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c9b-122">-DefaultProfile</span></span>
<span data-ttu-id="56c9b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56c9b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c9b-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="56c9b-124">-PublicCertData</span></span>
<span data-ttu-id="56c9b-125">Określa tekstową reprezentację głównego certyfikatu do dodania.</span><span class="sxs-lookup"><span data-stu-id="56c9b-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="56c9b-126">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="56c9b-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="56c9b-127">Po wykonaniu tej czynności zostanie wyświetlony wynik podobny do poniższego (należy zauważyć, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż skrót skrócony):-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Kończenie certyfikatu-----PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (-----Rozpocznij certyfikat-----) i ostatnim wierszem (----------końcowego certyfikatu) w pliku.</span><span class="sxs-lookup"><span data-stu-id="56c9b-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="56c9b-128">Możesz pobrać te dane za pomocą poleceń programu Windows PowerShell podobnych do tego: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="56c9b-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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

### <span data-ttu-id="56c9b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c9b-129">-ResourceGroupName</span></span>
<span data-ttu-id="56c9b-130">Określa nazwę grupy zasobów, do której przypisano certyfikat główny.</span><span class="sxs-lookup"><span data-stu-id="56c9b-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="56c9b-131">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56c9b-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="56c9b-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="56c9b-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="56c9b-133">Określa nazwę bramy sieci wirtualnej, do której został dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="56c9b-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="56c9b-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="56c9b-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="56c9b-135">Określa nazwę certyfikatu głównego klienta, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c9b-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="56c9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c9b-136">CommonParameters</span></span>
<span data-ttu-id="56c9b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c9b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c9b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c9b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56c9b-139">INPUTS</span></span>

### <span data-ttu-id="56c9b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56c9b-140">System.String</span></span>

## <span data-ttu-id="56c9b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56c9b-141">OUTPUTS</span></span>

### <span data-ttu-id="56c9b-142">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56c9b-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="56c9b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56c9b-143">NOTES</span></span>

## <span data-ttu-id="56c9b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56c9b-144">RELATED LINKS</span></span>

[<span data-ttu-id="56c9b-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56c9b-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="56c9b-146">Nowe — AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56c9b-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="56c9b-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56c9b-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


