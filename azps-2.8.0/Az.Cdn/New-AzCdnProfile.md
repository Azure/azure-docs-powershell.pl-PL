---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 7f62d12fbed217fa744ed5753c9234fb0e558caf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706544"
---
# <span data-ttu-id="34864-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34864-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="34864-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34864-102">SYNOPSIS</span></span>
<span data-ttu-id="34864-103">Tworzy profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="34864-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="34864-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34864-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34864-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34864-105">DESCRIPTION</span></span>
<span data-ttu-id="34864-106">Polecenie cmdlet **New-AzCdnProfile** tworzy profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="34864-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="34864-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34864-107">EXAMPLES</span></span>

## <span data-ttu-id="34864-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34864-108">PARAMETERS</span></span>

### <span data-ttu-id="34864-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34864-109">-DefaultProfile</span></span>
<span data-ttu-id="34864-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34864-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34864-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34864-111">-Location</span></span>
<span data-ttu-id="34864-112">Określa lokalizację zasobu profilu.</span><span class="sxs-lookup"><span data-stu-id="34864-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="34864-113">-Refilename</span><span class="sxs-lookup"><span data-stu-id="34864-113">-ProfileName</span></span>
<span data-ttu-id="34864-114">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="34864-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="34864-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34864-115">-ResourceGroupName</span></span>
<span data-ttu-id="34864-116">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="34864-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="34864-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="34864-117">-Sku</span></span>
<span data-ttu-id="34864-118">Określa jednostkę SKU profilu.</span><span class="sxs-lookup"><span data-stu-id="34864-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34864-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="34864-119">-Tag</span></span>
<span data-ttu-id="34864-120">Znaczniki, które mają zostać skojarzone z profilem usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="34864-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="34864-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34864-121">-Confirm</span></span>
<span data-ttu-id="34864-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34864-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34864-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34864-123">-WhatIf</span></span>
<span data-ttu-id="34864-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34864-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34864-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34864-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34864-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34864-126">CommonParameters</span></span>
<span data-ttu-id="34864-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34864-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34864-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34864-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34864-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34864-129">INPUTS</span></span>

### <span data-ttu-id="34864-130">System. String</span><span class="sxs-lookup"><span data-stu-id="34864-130">System.String</span></span>

## <span data-ttu-id="34864-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34864-131">OUTPUTS</span></span>

### <span data-ttu-id="34864-132">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="34864-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="34864-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34864-133">NOTES</span></span>

## <span data-ttu-id="34864-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34864-134">RELATED LINKS</span></span>

[<span data-ttu-id="34864-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34864-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="34864-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34864-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="34864-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34864-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


