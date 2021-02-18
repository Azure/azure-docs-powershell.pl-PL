---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201235"
---
# <span data-ttu-id="ac04a-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="ac04a-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="ac04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac04a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac04a-103">Resetuje zasady od dzierżawy w usłudze Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="ac04a-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="ac04a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac04a-104">SYNTAX</span></span>

### <span data-ttu-id="ac04a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac04a-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac04a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac04a-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac04a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac04a-107">DESCRIPTION</span></span>
<span data-ttu-id="ac04a-108">Polecenie Reset-AzAttestationPolicy resetuje zasady atestacji zdefiniowane przez użytkownika z dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="ac04a-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ac04a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac04a-109">EXAMPLES</span></span>

### <span data-ttu-id="ac04a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac04a-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="ac04a-111">Zresetuj zasady do wartości domyślnej testu *pshtestu* dostawcy poświadczenia dla *typu Tee SgxEntace.*</span><span class="sxs-lookup"><span data-stu-id="ac04a-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="ac04a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ac04a-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="ac04a-113">Jeśli test *pshtest* dostawcy poświadczenia jest skonfigurowany do używania odizolego modelu zaufania, zresetuj zasady do wartości domyślnej dla typu Tee *SgxEnnione,* uwzględniając podpisane zasady.</span><span class="sxs-lookup"><span data-stu-id="ac04a-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="ac04a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac04a-114">PARAMETERS</span></span>

### <span data-ttu-id="ac04a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac04a-115">-DefaultProfile</span></span>
<span data-ttu-id="ac04a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac04a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac04a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ac04a-117">-Name</span></span>
<span data-ttu-id="ac04a-118">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ac04a-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="ac04a-119">To polecenie cmdlet resetuje zasady atestacji dla dzierżawy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ac04a-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac04a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac04a-120">-PassThru</span></span>
<span data-ttu-id="ac04a-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="ac04a-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ac04a-122">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="ac04a-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ac04a-123">— Zasady</span><span class="sxs-lookup"><span data-stu-id="ac04a-123">-Policy</span></span>
<span data-ttu-id="ac04a-124">Określa token sieci Web JSON opisujący dokument zasad do zresetowania.</span><span class="sxs-lookup"><span data-stu-id="ac04a-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="ac04a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac04a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac04a-126">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="ac04a-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="ac04a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac04a-127">-ResourceId</span></span>
<span data-ttu-id="ac04a-128">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="ac04a-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="ac04a-129">— Tee</span><span class="sxs-lookup"><span data-stu-id="ac04a-129">-Tee</span></span>
<span data-ttu-id="ac04a-130">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="ac04a-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="ac04a-131">Obsługujemy cztery typy środowiska: SgxEnenae, OpenEnenae, CyResComponent i VBSEnkove.</span><span class="sxs-lookup"><span data-stu-id="ac04a-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="ac04a-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac04a-132">-Confirm</span></span>
<span data-ttu-id="ac04a-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac04a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac04a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac04a-134">-WhatIf</span></span>
<span data-ttu-id="ac04a-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac04a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac04a-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ac04a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac04a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac04a-137">CommonParameters</span></span>
<span data-ttu-id="ac04a-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac04a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac04a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac04a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac04a-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac04a-140">INPUTS</span></span>

### <span data-ttu-id="ac04a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ac04a-141">System.String</span></span>

## <span data-ttu-id="ac04a-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac04a-142">OUTPUTS</span></span>

### <span data-ttu-id="ac04a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac04a-143">System.Boolean</span></span>

## <span data-ttu-id="ac04a-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac04a-144">NOTES</span></span>

## <span data-ttu-id="ac04a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac04a-145">RELATED LINKS</span></span>
