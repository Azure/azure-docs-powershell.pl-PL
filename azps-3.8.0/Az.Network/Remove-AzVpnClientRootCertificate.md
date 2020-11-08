---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3288573719edac1f04b40ed624820397b4beebcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052916"
---
# <span data-ttu-id="793c9-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="793c9-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="793c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="793c9-102">SYNOPSIS</span></span>
<span data-ttu-id="793c9-103">Usuwa istniejący certyfikat główny klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="793c9-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="793c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="793c9-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="793c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="793c9-105">DESCRIPTION</span></span>
<span data-ttu-id="793c9-106">Polecenie cmdlet **Remove-AzVpnClientRootCertificate** usuwa określony certyfikat główny z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="793c9-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="793c9-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="793c9-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="793c9-108">Po usunięciu komputerów z certyfikatem głównym korzystającym z certyfikatu do celów uwierzytelnienia nie będzie już można połączyć się z bramą.</span><span class="sxs-lookup"><span data-stu-id="793c9-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="793c9-109">W przypadku korzystania z funkcji **Remove-AzVpnClientRootCertificate** należy podać zarówno nazwę certyfikatu, jak i tekstową reprezentację danych certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="793c9-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="793c9-110">Aby uzyskać więcej informacji na temat reprezentacji tekstu certyfikatu, zobacz opis parametru *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="793c9-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="793c9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="793c9-111">EXAMPLES</span></span>

### <span data-ttu-id="793c9-112">Przykład 1: Usuwanie certyfikatu głównego klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="793c9-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="793c9-113">W tym przykładzie usunięto certyfikat główny klienta o nazwie ContosoRootCertificate z ContosoVirtualGateway bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="793c9-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="793c9-114">W pierwszym poleceniu jest używane polecenie **Get-Content** , które pozwala uzyskać uprzednio wyeksportowany tekst przedstawiający reprezentację certyfikatu. Ta Reprezentacja tekstowa jest przechowywana w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="793c9-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="793c9-115">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu w $Text z wyjątkiem pierwszego wiersza i ostatniego wiersza.</span><span class="sxs-lookup"><span data-stu-id="793c9-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="793c9-116">Ten wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="793c9-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="793c9-117">W trzecim poleceniu są używane informacje przechowywane w zmiennej $CertificateText wraz z poleceniem cmdlet **Remove-AzVpnClientRootCertificate** w celu usunięcia certyfikatu z bramy.</span><span class="sxs-lookup"><span data-stu-id="793c9-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="793c9-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="793c9-118">PARAMETERS</span></span>

### <span data-ttu-id="793c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793c9-119">-DefaultProfile</span></span>
<span data-ttu-id="793c9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="793c9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="793c9-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="793c9-121">-PublicCertData</span></span>
<span data-ttu-id="793c9-122">Określa tekstową reprezentację głównego certyfikatu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="793c9-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="793c9-123">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="793c9-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="793c9-124">Powinno być wyświetlane dane wyjściowe podobne do poniższych (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż skrót skrócony):-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Kończenie certyfikatu-----PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (-----Rozpocznij certyfikat-----) i ostatnim wierszem (----------końcowego certyfikatu) w pliku.</span><span class="sxs-lookup"><span data-stu-id="793c9-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="793c9-125">Możesz pobrać PublicCertData za pomocą poleceń programu Windows PowerShell podobnych do tego: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="793c9-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="793c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="793c9-127">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="793c9-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="793c9-128">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="793c9-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="793c9-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="793c9-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="793c9-130">Określa nazwę bramy sieci wirtualnej, z której jest usuwany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="793c9-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="793c9-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="793c9-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="793c9-132">Określa nazwę certyfikatu głównego klienta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="793c9-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="793c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793c9-133">CommonParameters</span></span>
<span data-ttu-id="793c9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793c9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="793c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793c9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="793c9-136">INPUTS</span></span>

### <span data-ttu-id="793c9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="793c9-137">System.String</span></span>

## <span data-ttu-id="793c9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="793c9-138">OUTPUTS</span></span>

### <span data-ttu-id="793c9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="793c9-139">System.Boolean</span></span>

## <span data-ttu-id="793c9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="793c9-140">NOTES</span></span>

## <span data-ttu-id="793c9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="793c9-141">RELATED LINKS</span></span>

[<span data-ttu-id="793c9-142">Dodaj-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="793c9-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="793c9-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="793c9-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="793c9-144">Nowe — AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="793c9-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


