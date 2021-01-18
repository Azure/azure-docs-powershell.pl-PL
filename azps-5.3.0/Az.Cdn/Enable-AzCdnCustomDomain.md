---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502031"
---
# <span data-ttu-id="04aaf-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04aaf-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="04aaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="04aaf-103">Umożliwia włączenie niestandardowego HTTPS domeny (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="04aaf-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="04aaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04aaf-104">SYNTAX</span></span>

### <span data-ttu-id="04aaf-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04aaf-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04aaf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04aaf-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04aaf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04aaf-107">DESCRIPTION</span></span>
<span data-ttu-id="04aaf-108">Polecenie cmdlet **enable-AzCdnCustomDomain** włącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="04aaf-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="04aaf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04aaf-109">EXAMPLES</span></span>

### <span data-ttu-id="04aaf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04aaf-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="04aaf-111">Włącz dostarczanie za pomocą protokołu HTTPS domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="04aaf-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="04aaf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04aaf-112">PARAMETERS</span></span>

### <span data-ttu-id="04aaf-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="04aaf-113">-CustomDomainName</span></span>
<span data-ttu-id="04aaf-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="04aaf-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="04aaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04aaf-115">-DefaultProfile</span></span>
<span data-ttu-id="04aaf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04aaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04aaf-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="04aaf-117">-EndpointName</span></span>
<span data-ttu-id="04aaf-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="04aaf-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="04aaf-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04aaf-119">-InputObject</span></span>
<span data-ttu-id="04aaf-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="04aaf-120">The custom domain object.</span></span>

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

### <span data-ttu-id="04aaf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04aaf-121">-PassThru</span></span>
<span data-ttu-id="04aaf-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="04aaf-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="04aaf-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="04aaf-123">-ProfileName</span></span>
<span data-ttu-id="04aaf-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="04aaf-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="04aaf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04aaf-125">-ResourceGroupName</span></span>
<span data-ttu-id="04aaf-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="04aaf-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="04aaf-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04aaf-127">-Confirm</span></span>
<span data-ttu-id="04aaf-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04aaf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04aaf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04aaf-129">-WhatIf</span></span>
<span data-ttu-id="04aaf-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04aaf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04aaf-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04aaf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04aaf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04aaf-132">CommonParameters</span></span>
<span data-ttu-id="04aaf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04aaf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04aaf-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04aaf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04aaf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04aaf-135">INPUTS</span></span>

### <span data-ttu-id="04aaf-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04aaf-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="04aaf-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04aaf-137">OUTPUTS</span></span>

### <span data-ttu-id="04aaf-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04aaf-138">System.Boolean</span></span>

## <span data-ttu-id="04aaf-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04aaf-139">NOTES</span></span>

## <span data-ttu-id="04aaf-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04aaf-140">RELATED LINKS</span></span>
