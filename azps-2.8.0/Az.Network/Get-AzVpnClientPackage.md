---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 50919ba7857a57039e2afcdcd5cc4b469f91e612
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397955"
---
# <span data-ttu-id="486e4-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="486e4-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="486e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="486e4-102">SYNOPSIS</span></span>
<span data-ttu-id="486e4-103">Pobiera informacje o pakiecie klienta SIECI VPN.</span><span class="sxs-lookup"><span data-stu-id="486e4-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="486e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="486e4-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="486e4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="486e4-105">DESCRIPTION</span></span>
<span data-ttu-id="486e4-106">Polecenie **cmdlet Get-AzVpnClientPackage** pobiera informacje o pakietach klienta VPN dostępnych z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="486e4-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="486e4-107">Pakiety klientów zawierają dane konfiguracji, które umożliwiają klientowi nawiązaniu połączenia VPN z siecią wirtualną platformy Azure; aby można było nawiązaniu połączenia VPN, komputery klienckie muszą mieć zainstalowany właściwy pakiet konfiguracyjnych.</span><span class="sxs-lookup"><span data-stu-id="486e4-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="486e4-108">Różne pakiety konfiguracji są dostępne w zależności od wersji systemu Windows na komputerze klienckim (na przykład systemu Windows 7 lub Windows 10) i architektury procesora komputera klienckiego (AMD64 lub x86).</span><span class="sxs-lookup"><span data-stu-id="486e4-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="486e4-109">Podczas uruchamiania usługi **Get-AzVpnClientPackage** musisz określić typ architektury.</span><span class="sxs-lookup"><span data-stu-id="486e4-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="486e4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="486e4-110">EXAMPLES</span></span>

### <span data-ttu-id="486e4-111">Przykład 1. Uzyskiwanie informacji o pakiecie klienta VPN architektury procesora</span><span class="sxs-lookup"><span data-stu-id="486e4-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="486e4-112">To polecenie pobiera informacje o pakietach klienckich SIECI VPN AMD64 przechowywanych w wirtualnej bramie sieciowej o nazwie ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="486e4-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="486e4-113">Aby uzyskać informacje na temat pakietów klienta x86, ustaw wartość parametru *ProcessorArchitecture* na wartość x86.</span><span class="sxs-lookup"><span data-stu-id="486e4-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="486e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="486e4-114">PARAMETERS</span></span>

### <span data-ttu-id="486e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486e4-115">-DefaultProfile</span></span>
<span data-ttu-id="486e4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="486e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="486e4-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="486e4-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="486e4-118">Określa typ architektury procesora, dla których jest przeznaczony pakiet kliencki.</span><span class="sxs-lookup"><span data-stu-id="486e4-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="486e4-119">Prawidłowe wartości to Amd64 i X86.</span><span class="sxs-lookup"><span data-stu-id="486e4-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="486e4-121">Określa nazwę grupy zasobów, do których przypisano bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="486e4-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="486e4-122">Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.</span><span class="sxs-lookup"><span data-stu-id="486e4-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486e4-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="486e4-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="486e4-124">Określa nazwę bramy sieci wirtualnej, w której są przechowywane informacje o pakiecie klienta.</span><span class="sxs-lookup"><span data-stu-id="486e4-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486e4-125">CommonParameters</span></span>
<span data-ttu-id="486e4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486e4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="486e4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486e4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="486e4-128">INPUTS</span></span>

### <span data-ttu-id="486e4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="486e4-129">System.String</span></span>

## <span data-ttu-id="486e4-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="486e4-130">OUTPUTS</span></span>

### <span data-ttu-id="486e4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="486e4-131">System.String</span></span>

## <span data-ttu-id="486e4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="486e4-132">NOTES</span></span>

## <span data-ttu-id="486e4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="486e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="486e4-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="486e4-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



