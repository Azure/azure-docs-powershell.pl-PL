---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241082"
---
# <span data-ttu-id="0fab5-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0fab5-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="0fab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fab5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fab5-103">Dodaje certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="0fab5-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="0fab5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0fab5-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fab5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0fab5-105">DESCRIPTION</span></span>
<span data-ttu-id="0fab5-106">Polecenie **cmdlet Add-AzVpnClientRevokedCertificate** przypisuje certyfikat odwołania klienta do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0fab5-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="0fab5-107">Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="0fab5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="0fab5-108">Aby użyć tego polecenia cmdlet, należy zarówno określić nazwę certyfikatu, jak i nazwę usbprint certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0fab5-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="0fab5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0fab5-109">EXAMPLES</span></span>

### <span data-ttu-id="0fab5-110">Przykład 1. Dodawanie nowego certyfikatu odwołania klienta do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0fab5-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="0fab5-111">To polecenie dodaje nowy certyfikat odwołania klienta do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="0fab5-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="0fab5-112">Aby dodać certyfikat, musisz określić zarówno nazwę certyfikatu, jak i usbprint certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0fab5-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="0fab5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fab5-113">PARAMETERS</span></span>

### <span data-ttu-id="0fab5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fab5-114">-DefaultProfile</span></span>
<span data-ttu-id="0fab5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fab5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fab5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fab5-116">-ResourceGroupName</span></span>
<span data-ttu-id="0fab5-117">Określa nazwę grupy zasobów, do których przypisano bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0fab5-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="0fab5-118">Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.</span><span class="sxs-lookup"><span data-stu-id="0fab5-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="0fab5-119">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="0fab5-119">-Thumbprint</span></span>
<span data-ttu-id="0fab5-120">Określa identyfikator unikatowy dodawana certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0fab5-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="0fab5-121">Na przykład: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Możesz uzyskać informacje dotyczące kciuka dla certyfikatów, używając polecenia programu Windows PowerShell podobnego do `Get-ChildItem -Path Cert:\LocalMachine\Root` tego:</span><span class="sxs-lookup"><span data-stu-id="0fab5-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="0fab5-122">Poprzednie polecenie pobiera informacje dotyczące wszystkich certyfikatów komputerów lokalnych znalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="0fab5-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="0fab5-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0fab5-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0fab5-124">Określa nazwę bramy sieci wirtualnej, do której ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="0fab5-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="0fab5-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="0fab5-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="0fab5-126">Określa nazwę certyfikatu klienta sieci VPN do dodania.</span><span class="sxs-lookup"><span data-stu-id="0fab5-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="0fab5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fab5-127">CommonParameters</span></span>
<span data-ttu-id="0fab5-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fab5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fab5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fab5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fab5-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fab5-130">INPUTS</span></span>

### <span data-ttu-id="0fab5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0fab5-131">System.String</span></span>

## <span data-ttu-id="0fab5-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fab5-132">OUTPUTS</span></span>

### <span data-ttu-id="0fab5-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0fab5-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="0fab5-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0fab5-134">NOTES</span></span>

## <span data-ttu-id="0fab5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fab5-135">RELATED LINKS</span></span>

[<span data-ttu-id="0fab5-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0fab5-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="0fab5-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0fab5-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="0fab5-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0fab5-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


