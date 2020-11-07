---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 42de9254bc5bdaf31aa965aa7bdd1512cad361f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710391"
---
# <span data-ttu-id="4291b-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4291b-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4291b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4291b-102">SYNOPSIS</span></span>
<span data-ttu-id="4291b-103">Umożliwia włączenie niestandardowego HTTPS domeny (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="4291b-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="4291b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4291b-104">SYNTAX</span></span>

### <span data-ttu-id="4291b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4291b-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4291b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291b-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4291b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4291b-107">DESCRIPTION</span></span>
<span data-ttu-id="4291b-108">Polecenie cmdlet **enable-AzCdnCustomDomain** włącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="4291b-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="4291b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4291b-109">EXAMPLES</span></span>

### <span data-ttu-id="4291b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4291b-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="4291b-111">Włącz dostarczanie za pomocą protokołu HTTPS domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="4291b-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="4291b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4291b-112">PARAMETERS</span></span>

### <span data-ttu-id="4291b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4291b-113">-CustomDomainName</span></span>
<span data-ttu-id="4291b-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4291b-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="4291b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4291b-115">-DefaultProfile</span></span>
<span data-ttu-id="4291b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4291b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4291b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4291b-117">-EndpointName</span></span>
<span data-ttu-id="4291b-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4291b-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4291b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4291b-119">-InputObject</span></span>
<span data-ttu-id="4291b-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="4291b-120">The custom domain object.</span></span>

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

### <span data-ttu-id="4291b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4291b-121">-PassThru</span></span>
<span data-ttu-id="4291b-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="4291b-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="4291b-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="4291b-123">-ProfileName</span></span>
<span data-ttu-id="4291b-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4291b-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4291b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4291b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4291b-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4291b-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4291b-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4291b-127">-Confirm</span></span>
<span data-ttu-id="4291b-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4291b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4291b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4291b-129">-WhatIf</span></span>
<span data-ttu-id="4291b-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4291b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4291b-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4291b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4291b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4291b-132">CommonParameters</span></span>
<span data-ttu-id="4291b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4291b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4291b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4291b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4291b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4291b-135">INPUTS</span></span>

### <span data-ttu-id="4291b-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4291b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4291b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4291b-137">OUTPUTS</span></span>

### <span data-ttu-id="4291b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4291b-138">System.Boolean</span></span>

## <span data-ttu-id="4291b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4291b-139">NOTES</span></span>

## <span data-ttu-id="4291b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4291b-140">RELATED LINKS</span></span>
