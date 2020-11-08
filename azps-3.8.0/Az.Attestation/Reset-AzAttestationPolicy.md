---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051692"
---
# <span data-ttu-id="9c866-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="9c866-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="9c866-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c866-102">SYNOPSIS</span></span>
<span data-ttu-id="9c866-103">Resetuje zasady od dzierżawy na platformie Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="9c866-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="9c866-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c866-104">SYNTAX</span></span>

### <span data-ttu-id="9c866-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c866-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c866-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c866-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c866-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9c866-107">DESCRIPTION</span></span>
<span data-ttu-id="9c866-108">Polecenie cmdlet Reset-AzAttestationPolicy resetuje zasady zaświadczania zdefiniowane przez użytkownika od dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c866-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="9c866-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c866-109">EXAMPLES</span></span>

### <span data-ttu-id="9c866-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c866-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="9c866-111">Przywróć domyślną zasadę dla *Pshtest* dostawcy zaświadczania dla typu tee *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="9c866-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="9c866-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c866-112">PARAMETERS</span></span>

### <span data-ttu-id="9c866-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c866-113">-DefaultProfile</span></span>
<span data-ttu-id="9c866-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c866-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c866-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c866-115">-Name</span></span>
<span data-ttu-id="9c866-116">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9c866-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="9c866-117">To polecenie cmdlet resetuje zasady zaświadczania dla dzierżawy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9c866-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c866-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c866-118">-PassThru</span></span>
<span data-ttu-id="9c866-119">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="9c866-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9c866-120">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="9c866-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9c866-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="9c866-121">-Policy</span></span>
<span data-ttu-id="9c866-122">Określa token internetowy JSON opisujący dokument zasad do zresetowania.</span><span class="sxs-lookup"><span data-stu-id="9c866-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c866-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c866-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c866-124">Określa nazwę grupy zasobów dla dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="9c866-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="9c866-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c866-125">-ResourceId</span></span>
<span data-ttu-id="9c866-126">Określa identyfikator zasobu dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="9c866-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="9c866-127">-Tee</span><span class="sxs-lookup"><span data-stu-id="9c866-127">-Tee</span></span>
<span data-ttu-id="9c866-128">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="9c866-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="9c866-129">Obsługujemy cztery typy środowiska: SgxEnclave, OpenEnclave, CyResComponent i VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="9c866-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="9c866-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c866-130">-Confirm</span></span>
<span data-ttu-id="9c866-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c866-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c866-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c866-132">-WhatIf</span></span>
<span data-ttu-id="9c866-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c866-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c866-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c866-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c866-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c866-135">CommonParameters</span></span>
<span data-ttu-id="9c866-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c866-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c866-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c866-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c866-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c866-138">INPUTS</span></span>

### <span data-ttu-id="9c866-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c866-139">System.String</span></span>

## <span data-ttu-id="9c866-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c866-140">OUTPUTS</span></span>

### <span data-ttu-id="9c866-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c866-141">System.Boolean</span></span>

## <span data-ttu-id="9c866-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c866-142">NOTES</span></span>

## <span data-ttu-id="9c866-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c866-143">RELATED LINKS</span></span>
