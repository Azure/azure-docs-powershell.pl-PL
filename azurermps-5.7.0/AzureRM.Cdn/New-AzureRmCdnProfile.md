---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 5423844d7f466a827f3a452a05cf3999236198d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527021"
---
# <span data-ttu-id="69eb6-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="69eb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="69eb6-103">Tworzy profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="69eb6-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69eb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69eb6-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69eb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="69eb6-106">Polecenie cmdlet **New-AzureRmCdnProfile** tworzy profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="69eb6-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="69eb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69eb6-107">EXAMPLES</span></span>

## <span data-ttu-id="69eb6-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69eb6-108">PARAMETERS</span></span>

### <span data-ttu-id="69eb6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-109">-DefaultProfile</span></span>
<span data-ttu-id="69eb6-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="69eb6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69eb6-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="69eb6-111">-Location</span></span>
<span data-ttu-id="69eb6-112">Określa lokalizację zasobu profilu.</span><span class="sxs-lookup"><span data-stu-id="69eb6-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="69eb6-113">-Refilename</span><span class="sxs-lookup"><span data-stu-id="69eb6-113">-ProfileName</span></span>
<span data-ttu-id="69eb6-114">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="69eb6-114">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69eb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="69eb6-116">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="69eb6-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="69eb6-117">-Sku</span></span>
<span data-ttu-id="69eb6-118">Określa jednostkę SKU profilu.</span><span class="sxs-lookup"><span data-stu-id="69eb6-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="69eb6-119">-Tag</span></span>
<span data-ttu-id="69eb6-120">Znaczniki, które mają zostać skojarzone z profilem usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="69eb6-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69eb6-121">-Confirm</span></span>
<span data-ttu-id="69eb6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69eb6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69eb6-123">-WhatIf</span></span>
<span data-ttu-id="69eb6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69eb6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69eb6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69eb6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69eb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69eb6-126">CommonParameters</span></span>
<span data-ttu-id="69eb6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69eb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69eb6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69eb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69eb6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69eb6-129">INPUTS</span></span>

### <span data-ttu-id="69eb6-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="69eb6-130">None</span></span>
<span data-ttu-id="69eb6-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="69eb6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69eb6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69eb6-132">OUTPUTS</span></span>

### <span data-ttu-id="69eb6-133">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="69eb6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69eb6-134">NOTES</span></span>

## <span data-ttu-id="69eb6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69eb6-135">RELATED LINKS</span></span>

[<span data-ttu-id="69eb6-136">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-136">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="69eb6-137">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-137">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="69eb6-138">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69eb6-138">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


