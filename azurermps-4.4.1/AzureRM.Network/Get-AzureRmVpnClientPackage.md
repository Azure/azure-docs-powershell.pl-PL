---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: 0f6f9adfb75034dc106ba27f63de1ff826f5ab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554341"
---
# <span data-ttu-id="3e75a-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="3e75a-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="3e75a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e75a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e75a-103">Pobiera informacje o pakiecie klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="3e75a-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e75a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e75a-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e75a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e75a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e75a-106">Polecenie cmdlet **Get-AzureRmVpnClientPackage** pobiera informacje o pakietach klienckich sieci VPN dostępnych w wirtualnej bramie sieci.</span><span class="sxs-lookup"><span data-stu-id="3e75a-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="3e75a-107">Pakiety klienta zawierają dane konfiguracji umożliwiające komputerowi klienckiemu nawiązywania połączenia VPN z siecią wirtualną Azure. Aby nawiązać połączenie z siecią VPN, na komputerach klienckich musi być zainstalowany prawidłowy pakiet konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3e75a-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="3e75a-108">Różne pakiety konfiguracyjne są dostępne na podstawie wersji systemu Windows komputera klienckiego (na przykład system Windows 7 lub Windows 10) oraz w architekturze procesora komputera klienckiego (AMD64 lub x86).</span><span class="sxs-lookup"><span data-stu-id="3e75a-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="3e75a-109">Typ architektury należy określić podczas uruchamiania **Get-AzureRmVpnClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="3e75a-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="3e75a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e75a-110">EXAMPLES</span></span>

### <span data-ttu-id="3e75a-111">Przykład 1: uzyskiwanie informacji o pakiecie klienta sieci VPN architektura procesora</span><span class="sxs-lookup"><span data-stu-id="3e75a-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="3e75a-112">To polecenie pobiera informacje o pakietach klienckich sieci VPN AMD64 przechowywanych w bramy sieci wirtualnej o nazwie ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="3e75a-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="3e75a-113">Aby uzyskać informacje o pakietach klienta x86, ustaw wartość parametru *processorArchitecture* na wartość x86.</span><span class="sxs-lookup"><span data-stu-id="3e75a-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="3e75a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e75a-114">PARAMETERS</span></span>

### <span data-ttu-id="3e75a-115">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="3e75a-115">-ProcessorArchitecture</span></span>
<span data-ttu-id="3e75a-116">Określa typ architektury procesora, dla którego jest przeznaczony pakiet klienta.</span><span class="sxs-lookup"><span data-stu-id="3e75a-116">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="3e75a-117">Prawidłowe wartości to amd64 i x86.</span><span class="sxs-lookup"><span data-stu-id="3e75a-117">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="3e75a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e75a-118">-ResourceGroupName</span></span>
<span data-ttu-id="3e75a-119">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e75a-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="3e75a-120">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e75a-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3e75a-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3e75a-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3e75a-122">Określa nazwę bramy sieci wirtualnej, w której są przechowywane informacje o pakiecie klienta.</span><span class="sxs-lookup"><span data-stu-id="3e75a-122">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="3e75a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e75a-123">-DefaultProfile</span></span>
<span data-ttu-id="3e75a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e75a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e75a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e75a-125">CommonParameters</span></span>
<span data-ttu-id="3e75a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e75a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e75a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e75a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e75a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e75a-128">INPUTS</span></span>

### <span data-ttu-id="3e75a-129">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3e75a-129">String</span></span>
<span data-ttu-id="3e75a-130">Parametr "ResourceGroupName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="3e75a-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="3e75a-131">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3e75a-131">String</span></span>
<span data-ttu-id="3e75a-132">Parametr "VirtualNetworkGatewayName" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="3e75a-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3e75a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e75a-133">OUTPUTS</span></span>

###  
<span data-ttu-id="3e75a-134">Funkcja **Get-AzureRmVpnClientPackage** zwraca wystąpienia obiektu System. String.</span><span class="sxs-lookup"><span data-stu-id="3e75a-134">**Get-AzureRmVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="3e75a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e75a-135">NOTES</span></span>

## <span data-ttu-id="3e75a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e75a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3e75a-137">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3e75a-137">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3e75a-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="3e75a-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


