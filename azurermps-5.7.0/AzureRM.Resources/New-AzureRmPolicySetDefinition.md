---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547999"
---
# <span data-ttu-id="f89f1-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f89f1-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f89f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f89f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f89f1-103">Tworzy definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f89f1-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f89f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f89f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f89f1-106">Polecenie cmdlet **New-AzureRmPolicySetDefinition** umożliwia utworzenie definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="f89f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f89f1-107">EXAMPLES</span></span>

### <span data-ttu-id="f89f1-108">Przykład 1: Tworzenie definicji zestawu zasad przy użyciu pliku zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="f89f1-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f89f1-109">To polecenie tworzy definicję zestawu zasad o nazwie VMPolicyDefinition zawierającą definicje zasad określone w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="f89f1-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="f89f1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f89f1-110">PARAMETERS</span></span>

### <span data-ttu-id="f89f1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f89f1-111">-ApiVersion</span></span>
<span data-ttu-id="f89f1-112">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f89f1-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f89f1-113">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="f89f1-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89f1-114">-DefaultProfile</span></span>
<span data-ttu-id="f89f1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f89f1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f89f1-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="f89f1-116">-Description</span></span>
<span data-ttu-id="f89f1-117">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-117">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f89f1-118">-DisplayName</span></span>
<span data-ttu-id="f89f1-119">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-119">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f89f1-120">-Metadata</span></span>
<span data-ttu-id="f89f1-121">Metadane dotyczące definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-121">The metadata for policy set definition.</span></span> <span data-ttu-id="f89f1-122">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="f89f1-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f89f1-123">-Name</span></span>
<span data-ttu-id="f89f1-124">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-124">The policy set definition name.</span></span>

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

### <span data-ttu-id="f89f1-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f89f1-125">-Parameter</span></span>
<span data-ttu-id="f89f1-126">Deklaracja Parameters dla definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="f89f1-127">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="f89f1-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f89f1-128">-PolicyDefinition</span></span>
<span data-ttu-id="f89f1-129">Definicja zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="f89f1-129">The policy set definition.</span></span> <span data-ttu-id="f89f1-130">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicji zestawu zasad jako ciągu.</span><span class="sxs-lookup"><span data-stu-id="f89f1-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="f89f1-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f89f1-131">-Pre</span></span>
<span data-ttu-id="f89f1-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f89f1-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f89f1-133">-Confirm</span></span>
<span data-ttu-id="f89f1-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f89f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89f1-135">-WhatIf</span></span>
<span data-ttu-id="f89f1-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f89f1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f89f1-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f89f1-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89f1-138">CommonParameters</span></span>
<span data-ttu-id="f89f1-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f89f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89f1-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89f1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89f1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f89f1-141">INPUTS</span></span>

### <span data-ttu-id="f89f1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f89f1-142">System.String</span></span>

## <span data-ttu-id="f89f1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f89f1-143">OUTPUTS</span></span>

### <span data-ttu-id="f89f1-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f89f1-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f89f1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f89f1-145">NOTES</span></span>

## <span data-ttu-id="f89f1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f89f1-146">RELATED LINKS</span></span>
