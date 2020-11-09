---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308587"
---
# <span data-ttu-id="61bcf-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="61bcf-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="61bcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="61bcf-103">Dodaje osoby z listy zaufanych zasad dla dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61bcf-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="61bcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61bcf-104">SYNTAX</span></span>

### <span data-ttu-id="61bcf-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bcf-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bcf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bcf-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bcf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="61bcf-108">Polecenie cmdlet Add-AzAttestationPolicySigner umożliwia dodanie osoby podpisującej zaufane zasady dla dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61bcf-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="61bcf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61bcf-109">EXAMPLES</span></span>

### <span data-ttu-id="61bcf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61bcf-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="61bcf-111">Dodaj zaufaną podpisującego dostawcę Atteestation o nazwie *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="61bcf-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="61bcf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61bcf-112">PARAMETERS</span></span>

### <span data-ttu-id="61bcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bcf-113">-DefaultProfile</span></span>
<span data-ttu-id="61bcf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61bcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61bcf-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61bcf-115">-Name</span></span>
<span data-ttu-id="61bcf-116">Określa nazwę dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="61bcf-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="61bcf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bcf-117">-ResourceGroupName</span></span>
<span data-ttu-id="61bcf-118">Określa nazwę grupy zasobów dla dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="61bcf-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="61bcf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61bcf-119">-ResourceId</span></span>
<span data-ttu-id="61bcf-120">Określa identyfikator zasobu dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="61bcf-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="61bcf-121">-Osoba podpisująca</span><span class="sxs-lookup"><span data-stu-id="61bcf-121">-Signer</span></span>
<span data-ttu-id="61bcf-122">Określa token sieci Web JSON RFC7519 zawierający oświadczenie o nazwie "Maa-policyCertificate", którego wartość jest kluczem sieci Web kodu JSON usługi RFC7517, który zawiera nowy zaufany klucz podpisywania do dodania.</span><span class="sxs-lookup"><span data-stu-id="61bcf-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="61bcf-123">RFC7519 JWT musi być podpisany jednym z istniejących zaufanych kluczy podpisywania.</span><span class="sxs-lookup"><span data-stu-id="61bcf-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="61bcf-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61bcf-124">-Confirm</span></span>
<span data-ttu-id="61bcf-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bcf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bcf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bcf-126">-WhatIf</span></span>
<span data-ttu-id="61bcf-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bcf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bcf-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61bcf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bcf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bcf-129">CommonParameters</span></span>
<span data-ttu-id="61bcf-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bcf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bcf-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61bcf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bcf-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61bcf-132">INPUTS</span></span>

### <span data-ttu-id="61bcf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="61bcf-133">System.String</span></span>

## <span data-ttu-id="61bcf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61bcf-134">OUTPUTS</span></span>

### <span data-ttu-id="61bcf-135">Microsoft. Azure. Commands. zaświadczanie. modele. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="61bcf-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="61bcf-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61bcf-136">NOTES</span></span>

## <span data-ttu-id="61bcf-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61bcf-137">RELATED LINKS</span></span>
