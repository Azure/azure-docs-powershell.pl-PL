---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353290"
---
# <span data-ttu-id="c4296-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="c4296-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="c4296-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4296-102">SYNOPSIS</span></span>
<span data-ttu-id="c4296-103">Resetuje zasady od dzierżawy na platformie Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="c4296-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="c4296-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4296-104">SYNTAX</span></span>

### <span data-ttu-id="c4296-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4296-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4296-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4296-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4296-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4296-107">DESCRIPTION</span></span>
<span data-ttu-id="c4296-108">Polecenie cmdlet Reset-AzAttestationPolicy resetuje zasady zaświadczania zdefiniowane przez użytkownika od dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4296-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c4296-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4296-109">EXAMPLES</span></span>

### <span data-ttu-id="c4296-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4296-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="c4296-111">Przywróć domyślną zasadę dla *Pshtest* dostawcy zaświadczania dla typu tee *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="c4296-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="c4296-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4296-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="c4296-113">Jeśli *Pshtest* dostawcy zaświadczania jest skonfigurowany do korzystania z izolowanego modelu zaufania, Przywróć domyślną zasadę dla typu tee *SgxEnclave* , dołączając zasady podpisane.</span><span class="sxs-lookup"><span data-stu-id="c4296-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="c4296-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4296-114">PARAMETERS</span></span>

### <span data-ttu-id="c4296-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4296-115">-DefaultProfile</span></span>
<span data-ttu-id="c4296-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4296-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4296-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4296-117">-Name</span></span>
<span data-ttu-id="c4296-118">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c4296-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="c4296-119">To polecenie cmdlet resetuje zasady zaświadczania dla dzierżawy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c4296-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4296-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4296-120">-PassThru</span></span>
<span data-ttu-id="c4296-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="c4296-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c4296-122">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c4296-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c4296-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="c4296-123">-Policy</span></span>
<span data-ttu-id="c4296-124">Określa token internetowy JSON opisujący dokument zasad do zresetowania.</span><span class="sxs-lookup"><span data-stu-id="c4296-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="c4296-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4296-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4296-126">Określa nazwę grupy zasobów dla dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="c4296-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="c4296-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4296-127">-ResourceId</span></span>
<span data-ttu-id="c4296-128">Określa identyfikator zasobu dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="c4296-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="c4296-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="c4296-129">-Tee</span></span>
<span data-ttu-id="c4296-130">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="c4296-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="c4296-131">Obsługujemy cztery typy środowiska: SgxEnclave, OpenEnclave, CyResComponent i VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="c4296-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="c4296-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4296-132">-Confirm</span></span>
<span data-ttu-id="c4296-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4296-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4296-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4296-134">-WhatIf</span></span>
<span data-ttu-id="c4296-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4296-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4296-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4296-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4296-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4296-137">CommonParameters</span></span>
<span data-ttu-id="c4296-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4296-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4296-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4296-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4296-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4296-140">INPUTS</span></span>

### <span data-ttu-id="c4296-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c4296-141">System.String</span></span>

## <span data-ttu-id="c4296-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4296-142">OUTPUTS</span></span>

### <span data-ttu-id="c4296-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4296-143">System.Boolean</span></span>

## <span data-ttu-id="c4296-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4296-144">NOTES</span></span>

## <span data-ttu-id="c4296-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4296-145">RELATED LINKS</span></span>
