---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525793"
---
# <span data-ttu-id="9f937-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f937-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="9f937-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f937-102">SYNOPSIS</span></span>
<span data-ttu-id="9f937-103">Tworzy wystąpienie PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9f937-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f937-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f937-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f937-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9f937-105">DESCRIPTION</span></span>
<span data-ttu-id="9f937-106">Polecenie cmdlet **New-AzureRmApiManagementVirtualNetwork** jest poleceniem pomagającym w celu utworzenia wystąpienia **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="9f937-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="9f937-107">To polecenie jest używane przy użyciu polecenia cmdlet **Set-AzureRMApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="9f937-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="9f937-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f937-108">EXAMPLES</span></span>

### <span data-ttu-id="9f937-109">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9f937-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="9f937-110">W tym przykładzie jest tworzona Sieć wirtualna, a następnie jest wywoływana funkcja cmdlet **Set-AzureRmApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="9f937-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="9f937-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f937-111">PARAMETERS</span></span>

### <span data-ttu-id="9f937-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9f937-112">-Location</span></span>
<span data-ttu-id="9f937-113">Określa lokalizację sieci wirtualnej, w której to polecenie cmdlet tworzy wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="9f937-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="9f937-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9f937-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f937-115">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="9f937-115">North Central US</span></span>
- <span data-ttu-id="9f937-116">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="9f937-116">South Central US</span></span>
- <span data-ttu-id="9f937-117">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="9f937-117">Central US</span></span>
- <span data-ttu-id="9f937-118">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="9f937-118">West Europe</span></span>
- <span data-ttu-id="9f937-119">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="9f937-119">North Europe</span></span>
- <span data-ttu-id="9f937-120">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="9f937-120">West US</span></span>
- <span data-ttu-id="9f937-121">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="9f937-121">East US</span></span>
- <span data-ttu-id="9f937-122">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="9f937-122">East US 2</span></span>
- <span data-ttu-id="9f937-123">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="9f937-123">Japan East</span></span>
- <span data-ttu-id="9f937-124">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="9f937-124">Japan West</span></span>
- <span data-ttu-id="9f937-125">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="9f937-125">Brazil South</span></span>
- <span data-ttu-id="9f937-126">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9f937-126">Southeast Asia</span></span>
- <span data-ttu-id="9f937-127">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9f937-127">East Asia</span></span>
- <span data-ttu-id="9f937-128">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="9f937-128">Australia East</span></span>
- <span data-ttu-id="9f937-129">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="9f937-129">Australia Southeast</span></span>

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

### <span data-ttu-id="9f937-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="9f937-130">-SubnetResourceId</span></span>
<span data-ttu-id="9f937-131">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9f937-131">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="9f937-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f937-132">-DefaultProfile</span></span>
<span data-ttu-id="9f937-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f937-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f937-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f937-134">CommonParameters</span></span>
<span data-ttu-id="9f937-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f937-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f937-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f937-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f937-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f937-137">INPUTS</span></span>

## <span data-ttu-id="9f937-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f937-138">OUTPUTS</span></span>

### <span data-ttu-id="9f937-139">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f937-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="9f937-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f937-140">NOTES</span></span>

## <span data-ttu-id="9f937-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f937-141">RELATED LINKS</span></span>

