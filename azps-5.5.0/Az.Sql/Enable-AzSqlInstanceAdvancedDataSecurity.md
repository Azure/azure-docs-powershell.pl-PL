---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 03f393daf629329ff90a6606760a0c7bc70ad788
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178522"
---
# <span data-ttu-id="49c06-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="49c06-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="49c06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c06-102">SYNOPSIS</span></span>
<span data-ttu-id="49c06-103">Włącza zaawansowane zabezpieczenia danych w wystąpieniu zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="49c06-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="49c06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49c06-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49c06-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="49c06-105">DESCRIPTION</span></span>
<span data-ttu-id="49c06-106">Polecenie **cmdlet Enable-AzSqlInstanceAdvancedDataSecurity** umożliwia włączenie zaawansowanego zabezpieczeń danych w wystąpieniu zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="49c06-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="49c06-107">Advanced Data Security to ujednolicony pakiet zabezpieczeń, który zawiera klasyfikację danych, ocenę luk i zaawansowaną ochronę przed zagrożeniami dla zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="49c06-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="49c06-108">(Zostanie automatycznie utworzone nowe konto magazynu w celu zapisania oceny luk w zabezpieczeniach.</span><span class="sxs-lookup"><span data-stu-id="49c06-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="49c06-109">Jeśli do tego celu wcześniej utworzono konto magazynu, będzie ono używane zamiast tego)</span><span class="sxs-lookup"><span data-stu-id="49c06-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="49c06-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49c06-110">EXAMPLES</span></span>

### <span data-ttu-id="49c06-111">Przykład 1. Włączanie zaawansowanego zabezpieczeń danych zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="49c06-111">Example 1: Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="49c06-112">Przykład 2. Włączanie zaawansowanego zabezpieczeń danych wystąpienia zarządzanego z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="49c06-112">Example 2: Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="49c06-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="49c06-113">Example 3</span></span>

<span data-ttu-id="49c06-114">Włącza zaawansowane zabezpieczenia danych w wystąpieniu zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="49c06-114">Enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="49c06-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="49c06-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Enable-AzSqlInstanceAdvancedDataSecurity -DoNotConfigureVulnerabilityAssessment -InstanceName 'ContosoManagedInstanceName' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="49c06-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c06-116">PARAMETERS</span></span>

### <span data-ttu-id="49c06-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="49c06-117">-AsJob</span></span>
<span data-ttu-id="49c06-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49c06-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49c06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c06-119">-DefaultProfile</span></span>
<span data-ttu-id="49c06-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49c06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c06-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="49c06-121">-DeploymentName</span></span>
<span data-ttu-id="49c06-122">Dostarczanie niestandardowej nazwy dla wdrożenia Zaawansowane zabezpieczenia danych</span><span class="sxs-lookup"><span data-stu-id="49c06-122">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="49c06-123">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="49c06-123">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="49c06-124">Nie włączaj automatycznie oceny luk (nie spowoduje to utworzenia konta magazynu)</span><span class="sxs-lookup"><span data-stu-id="49c06-124">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="49c06-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49c06-125">-InputObject</span></span>
<span data-ttu-id="49c06-126">Obiekt zarządzanego wystąpienia do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="49c06-126">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49c06-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="49c06-127">-InstanceName</span></span>
<span data-ttu-id="49c06-128">Nazwa zarządzanego wystąpienia usługi SQL Database.</span><span class="sxs-lookup"><span data-stu-id="49c06-128">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c06-129">-ResourceGroupName</span></span>
<span data-ttu-id="49c06-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49c06-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c06-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49c06-131">-Confirm</span></span>
<span data-ttu-id="49c06-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49c06-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c06-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c06-133">-WhatIf</span></span>
<span data-ttu-id="49c06-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49c06-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c06-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49c06-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c06-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c06-136">CommonParameters</span></span>
<span data-ttu-id="49c06-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c06-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c06-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c06-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c06-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49c06-139">INPUTS</span></span>

### <span data-ttu-id="49c06-140">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="49c06-140">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="49c06-141">System.String</span><span class="sxs-lookup"><span data-stu-id="49c06-141">System.String</span></span>

## <span data-ttu-id="49c06-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49c06-142">OUTPUTS</span></span>

### <span data-ttu-id="49c06-143">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="49c06-143">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="49c06-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49c06-144">NOTES</span></span>

## <span data-ttu-id="49c06-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49c06-145">RELATED LINKS</span></span>
