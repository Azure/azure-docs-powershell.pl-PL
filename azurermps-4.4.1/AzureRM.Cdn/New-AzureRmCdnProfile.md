---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550067"
---
# <span data-ttu-id="5860a-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="5860a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5860a-102">SYNOPSIS</span></span>
<span data-ttu-id="5860a-103">Tworzy profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="5860a-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5860a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5860a-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5860a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5860a-105">DESCRIPTION</span></span>
<span data-ttu-id="5860a-106">Polecenie cmdlet **New-AzureRmCdnProfile** tworzy profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="5860a-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5860a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5860a-107">EXAMPLES</span></span>

## <span data-ttu-id="5860a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5860a-108">PARAMETERS</span></span>

### <span data-ttu-id="5860a-109">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5860a-109">-Location</span></span>
<span data-ttu-id="5860a-110">Określa lokalizację zasobu profilu.</span><span class="sxs-lookup"><span data-stu-id="5860a-110">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="5860a-111">-Refilename</span><span class="sxs-lookup"><span data-stu-id="5860a-111">-ProfileName</span></span>
<span data-ttu-id="5860a-112">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="5860a-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="5860a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5860a-113">-ResourceGroupName</span></span>
<span data-ttu-id="5860a-114">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="5860a-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5860a-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="5860a-115">-Sku</span></span>
<span data-ttu-id="5860a-116">Określa jednostkę SKU profilu.</span><span class="sxs-lookup"><span data-stu-id="5860a-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5860a-117">-Tagi</span><span class="sxs-lookup"><span data-stu-id="5860a-117">-Tags</span></span>
<span data-ttu-id="5860a-118">Sepcifies tablicę skrótów tagów, które są skojarzone z tym profilem.</span><span class="sxs-lookup"><span data-stu-id="5860a-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5860a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5860a-119">-Confirm</span></span>
<span data-ttu-id="5860a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5860a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5860a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5860a-121">-WhatIf</span></span>
<span data-ttu-id="5860a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5860a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5860a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5860a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5860a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-124">-DefaultProfile</span></span>
<span data-ttu-id="5860a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5860a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5860a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5860a-126">CommonParameters</span></span>
<span data-ttu-id="5860a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5860a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5860a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5860a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5860a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5860a-129">INPUTS</span></span>

## <span data-ttu-id="5860a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5860a-130">OUTPUTS</span></span>

### <span data-ttu-id="5860a-131">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5860a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5860a-132">NOTES</span></span>

## <span data-ttu-id="5860a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5860a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5860a-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="5860a-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="5860a-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5860a-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


