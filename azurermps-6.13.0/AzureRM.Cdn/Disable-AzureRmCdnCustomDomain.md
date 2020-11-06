---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547543"
---
# <span data-ttu-id="cf2ac-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cf2ac-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="cf2ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2ac-103">Wyłączenie niestandardowego protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf2ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf2ac-104">SYNTAX</span></span>

### <span data-ttu-id="cf2ac-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf2ac-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf2ac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf2ac-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf2ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="cf2ac-108">Polecenie cmdlet **disable-AzureRmCdnCustomDomain** wyłącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="cf2ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf2ac-109">EXAMPLES</span></span>

### <span data-ttu-id="cf2ac-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf2ac-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="cf2ac-111">Wyłącz dostarczanie https domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="cf2ac-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf2ac-112">PARAMETERS</span></span>

### <span data-ttu-id="cf2ac-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cf2ac-113">-CustomDomainName</span></span>
<span data-ttu-id="cf2ac-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-114">Azure CDN custom domain display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2ac-115">-DefaultProfile</span></span>
<span data-ttu-id="cf2ac-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf2ac-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cf2ac-117">-EndpointName</span></span>
<span data-ttu-id="cf2ac-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf2ac-119">-InputObject</span></span>
<span data-ttu-id="cf2ac-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf2ac-121">-PassThru</span></span>
<span data-ttu-id="cf2ac-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="cf2ac-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="cf2ac-123">-ProfileName</span></span>
<span data-ttu-id="cf2ac-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-124">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf2ac-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-126">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf2ac-127">-Confirm</span></span>
<span data-ttu-id="cf2ac-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2ac-129">-WhatIf</span></span>
<span data-ttu-id="cf2ac-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf2ac-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2ac-132">CommonParameters</span></span>
<span data-ttu-id="cf2ac-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2ac-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2ac-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf2ac-135">INPUTS</span></span>

### <span data-ttu-id="cf2ac-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cf2ac-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="cf2ac-137">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf2ac-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cf2ac-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf2ac-138">OUTPUTS</span></span>

### <span data-ttu-id="cf2ac-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf2ac-139">System.Boolean</span></span>

## <span data-ttu-id="cf2ac-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf2ac-140">NOTES</span></span>

## <span data-ttu-id="cf2ac-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf2ac-141">RELATED LINKS</span></span>
