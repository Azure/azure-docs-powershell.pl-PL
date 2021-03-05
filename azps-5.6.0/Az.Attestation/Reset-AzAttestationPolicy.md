---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966794"
---
# <span data-ttu-id="37e58-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="37e58-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="37e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e58-102">SYNOPSIS</span></span>
<span data-ttu-id="37e58-103">Resetuje zasady od dzierżawy w usłudze Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="37e58-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="37e58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37e58-104">SYNTAX</span></span>

### <span data-ttu-id="37e58-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e58-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e58-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37e58-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e58-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="37e58-107">DESCRIPTION</span></span>
<span data-ttu-id="37e58-108">Polecenie Reset-AzAttestationPolicy resetuje zasady atestacji zdefiniowane przez użytkownika z dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="37e58-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="37e58-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37e58-109">EXAMPLES</span></span>

### <span data-ttu-id="37e58-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37e58-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="37e58-111">Zresetuj zasady do wartości domyślnej testu *pshtestu* dostawcy poświadczenia dla *typu Tee SgxEntace.*</span><span class="sxs-lookup"><span data-stu-id="37e58-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="37e58-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="37e58-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="37e58-113">Jeśli test *pshtest* dostawcy poświadczenia jest skonfigurowany do używania modelu zaufania odizolego, zresetuj zasady do wartości domyślnej dla typu Tee *SgxEnają,* uwzględniając podpisane zasady.</span><span class="sxs-lookup"><span data-stu-id="37e58-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="37e58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37e58-114">PARAMETERS</span></span>

### <span data-ttu-id="37e58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e58-115">-DefaultProfile</span></span>
<span data-ttu-id="37e58-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37e58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e58-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37e58-117">-Name</span></span>
<span data-ttu-id="37e58-118">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="37e58-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="37e58-119">To polecenie cmdlet resetuje zasady atestacji dla dzierżawy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="37e58-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="37e58-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37e58-120">-PassThru</span></span>
<span data-ttu-id="37e58-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="37e58-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="37e58-122">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="37e58-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="37e58-123">— Zasady</span><span class="sxs-lookup"><span data-stu-id="37e58-123">-Policy</span></span>
<span data-ttu-id="37e58-124">Określa token sieci Web JSON opisujący dokument zasad do zresetowania.</span><span class="sxs-lookup"><span data-stu-id="37e58-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="37e58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e58-125">-ResourceGroupName</span></span>
<span data-ttu-id="37e58-126">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="37e58-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="37e58-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37e58-127">-ResourceId</span></span>
<span data-ttu-id="37e58-128">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="37e58-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="37e58-129">- Tee</span><span class="sxs-lookup"><span data-stu-id="37e58-129">-Tee</span></span>
<span data-ttu-id="37e58-130">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="37e58-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="37e58-131">Obsługujemy cztery typy środowiska: SgxEnenae, OpenEnenae, CyResComponent i VBSEnżdże.</span><span class="sxs-lookup"><span data-stu-id="37e58-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="37e58-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37e58-132">-Confirm</span></span>
<span data-ttu-id="37e58-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37e58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e58-134">-WhatIf</span></span>
<span data-ttu-id="37e58-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e58-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37e58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e58-137">CommonParameters</span></span>
<span data-ttu-id="37e58-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e58-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37e58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e58-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e58-140">INPUTS</span></span>

### <span data-ttu-id="37e58-141">System.String</span><span class="sxs-lookup"><span data-stu-id="37e58-141">System.String</span></span>

## <span data-ttu-id="37e58-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e58-142">OUTPUTS</span></span>

### <span data-ttu-id="37e58-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37e58-143">System.Boolean</span></span>

## <span data-ttu-id="37e58-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37e58-144">NOTES</span></span>

## <span data-ttu-id="37e58-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e58-145">RELATED LINKS</span></span>
