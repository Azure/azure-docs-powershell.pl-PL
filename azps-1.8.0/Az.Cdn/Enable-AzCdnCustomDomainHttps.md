---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 87c6928b6b1a8863bdde7126b782d07d4c496207
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710390"
---
# <span data-ttu-id="2f4f1-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="2f4f1-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="2f4f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4f1-103">Umożliwia włączenie niestandardowego protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="2f4f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f4f1-104">SYNTAX</span></span>

### <span data-ttu-id="2f4f1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2f4f1-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f4f1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4f1-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f4f1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4f1-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4f1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2f4f1-108">DESCRIPTION</span></span>
<span data-ttu-id="2f4f1-109">Polecenie cmdlet **enable-AzCdnCustomDomainHttps** włącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="2f4f1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f4f1-110">EXAMPLES</span></span>

### <span data-ttu-id="2f4f1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f4f1-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="2f4f1-112">Włącz Zabezpieczanie dostarczania domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="2f4f1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f4f1-113">PARAMETERS</span></span>

### <span data-ttu-id="2f4f1-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2f4f1-114">-CustomDomainName</span></span>
<span data-ttu-id="2f4f1-115">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="2f4f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4f1-116">-DefaultProfile</span></span>
<span data-ttu-id="2f4f1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f4f1-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2f4f1-118">-EndpointName</span></span>
<span data-ttu-id="2f4f1-119">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2f4f1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f4f1-120">-InputObject</span></span>
<span data-ttu-id="2f4f1-121">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-121">The custom domain object.</span></span>

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

### <span data-ttu-id="2f4f1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f4f1-122">-PassThru</span></span>
<span data-ttu-id="2f4f1-123">Zwraca obiekt, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-123">Return object if specified.</span></span>

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

### <span data-ttu-id="2f4f1-124">-Refilename</span><span class="sxs-lookup"><span data-stu-id="2f4f1-124">-ProfileName</span></span>
<span data-ttu-id="2f4f1-125">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2f4f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f4f1-127">Grupa zasobów profilu usługi Azure CDN</span><span class="sxs-lookup"><span data-stu-id="2f4f1-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="2f4f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f4f1-128">-ResourceId</span></span>
<span data-ttu-id="2f4f1-129">Identyfikator zasobu domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="2f4f1-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f1-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f4f1-130">-Confirm</span></span>
<span data-ttu-id="2f4f1-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4f1-132">-WhatIf</span></span>
<span data-ttu-id="2f4f1-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4f1-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4f1-135">CommonParameters</span></span>
<span data-ttu-id="2f4f1-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4f1-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4f1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4f1-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f4f1-138">INPUTS</span></span>

### <span data-ttu-id="2f4f1-139">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2f4f1-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="2f4f1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f4f1-140">System.String</span></span>

## <span data-ttu-id="2f4f1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f4f1-141">OUTPUTS</span></span>

### <span data-ttu-id="2f4f1-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f4f1-142">System.Boolean</span></span>

## <span data-ttu-id="2f4f1-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f4f1-143">NOTES</span></span>

## <span data-ttu-id="2f4f1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f4f1-144">RELATED LINKS</span></span>
