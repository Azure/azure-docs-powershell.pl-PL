---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: d4f04c47c37446b6521c122b7551263809bb1c49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972234"
---
# <span data-ttu-id="8f999-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="8f999-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="8f999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f999-102">SYNOPSIS</span></span>
<span data-ttu-id="8f999-103">Dodaje zaufanego podpiszącego zasady dla dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="8f999-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="8f999-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f999-104">SYNTAX</span></span>

### <span data-ttu-id="8f999-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f999-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f999-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f999-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f999-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f999-107">DESCRIPTION</span></span>
<span data-ttu-id="8f999-108">Polecenie Add-AzAttestationPolicySigner cmdlet dodaje zaufanego podpiszącego zasady dla dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="8f999-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="8f999-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f999-109">EXAMPLES</span></span>

### <span data-ttu-id="8f999-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f999-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="8f999-111">Dodaj zaufanego podpisatora dla dostawcy usług atestacji o nazwie *pshtest.*</span><span class="sxs-lookup"><span data-stu-id="8f999-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="8f999-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f999-112">PARAMETERS</span></span>

### <span data-ttu-id="8f999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f999-113">-DefaultProfile</span></span>
<span data-ttu-id="8f999-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f999-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f999-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8f999-115">-Name</span></span>
<span data-ttu-id="8f999-116">Określa nazwę dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="8f999-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f999-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f999-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f999-118">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="8f999-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f999-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f999-119">-ResourceId</span></span>
<span data-ttu-id="8f999-120">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="8f999-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f999-121">— Podpis</span><span class="sxs-lookup"><span data-stu-id="8f999-121">-Signer</span></span>
<span data-ttu-id="8f999-122">Określa token sieci Web JSON JSON RFC7519 zawierający żądanie o nazwie "maa-policyCertificate", którego wartość to klucz sieci Web JSON RFC7517, który zawiera nowy zaufany klucz podpisywania do dodania.</span><span class="sxs-lookup"><span data-stu-id="8f999-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="8f999-123">JWT RFC7519 musi być podpisany przy użyciu jednego z istniejących zaufanych kluczy podpisywania.</span><span class="sxs-lookup"><span data-stu-id="8f999-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="8f999-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f999-124">-Confirm</span></span>
<span data-ttu-id="8f999-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f999-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f999-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f999-126">-WhatIf</span></span>
<span data-ttu-id="8f999-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f999-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f999-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f999-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f999-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f999-129">CommonParameters</span></span>
<span data-ttu-id="8f999-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f999-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f999-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f999-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f999-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f999-132">INPUTS</span></span>

### <span data-ttu-id="8f999-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8f999-133">System.String</span></span>

## <span data-ttu-id="8f999-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f999-134">OUTPUTS</span></span>

### <span data-ttu-id="8f999-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="8f999-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="8f999-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f999-136">NOTES</span></span>

## <span data-ttu-id="8f999-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f999-137">RELATED LINKS</span></span>
