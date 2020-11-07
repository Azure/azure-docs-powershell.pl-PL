---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895929"
---
# <span data-ttu-id="bdbc2-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="bdbc2-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="bdbc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbc2-103">Włącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="bdbc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdbc2-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdbc2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bdbc2-105">DESCRIPTION</span></span>
<span data-ttu-id="bdbc2-106">Polecenie cmdlet **enable-AzSqlInstanceAdvancedDataSecurity** włącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="bdbc2-107">Zaawansowane zabezpieczenia danych to ujednolicony pakiet zabezpieczeń, który obejmuje klasyfikację danych, ocenę luk i zaawansowaną ochronę przed zagrożeniami w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="bdbc2-108">(Nowe konto magazynu zostanie automatycznie utworzone w celu zapisania ocen dotyczących luk.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="bdbc2-109">Jeśli w tym celu utworzono wcześniej konto magazynu, zamiast tego zostanie użyte to polecenie.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="bdbc2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdbc2-110">EXAMPLES</span></span>

### <span data-ttu-id="bdbc2-111">Przykład 1-Włączanie zaawansowanych zabezpieczeń danych wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="bdbc2-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="bdbc2-112">Przykład 2 — Włączanie zaawansowanego zabezpieczenia danych wystąpienia zarządzanego z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="bdbc2-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="bdbc2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdbc2-113">PARAMETERS</span></span>

### <span data-ttu-id="bdbc2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdbc2-114">-AsJob</span></span>
<span data-ttu-id="bdbc2-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bdbc2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdbc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbc2-116">-DefaultProfile</span></span>
<span data-ttu-id="bdbc2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdbc2-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="bdbc2-118">-DeploymentName</span></span>
<span data-ttu-id="bdbc2-119">Podaj nazwę niestandardową dla zaawansowanego wdrożenia zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="bdbc2-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="bdbc2-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="bdbc2-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="bdbc2-121">Nie włączaj automatycznie oceny luki (nie spowoduje to utworzenia konta magazynu)</span><span class="sxs-lookup"><span data-stu-id="bdbc2-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="bdbc2-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdbc2-122">-InputObject</span></span>
<span data-ttu-id="bdbc2-123">Obiekt wystąpienia zarządzanego, który ma być używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="bdbc2-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="bdbc2-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bdbc2-124">-InstanceName</span></span>
<span data-ttu-id="bdbc2-125">Nazwa wystąpienia zarządzanego bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="bdbc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdbc2-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdbc2-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdbc2-128">-Confirm</span></span>
<span data-ttu-id="bdbc2-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbc2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbc2-130">-WhatIf</span></span>
<span data-ttu-id="bdbc2-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbc2-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbc2-133">CommonParameters</span></span>
<span data-ttu-id="bdbc2-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbc2-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdbc2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbc2-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdbc2-136">INPUTS</span></span>

### <span data-ttu-id="bdbc2-137">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="bdbc2-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="bdbc2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bdbc2-138">System.String</span></span>

## <span data-ttu-id="bdbc2-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdbc2-139">OUTPUTS</span></span>

### <span data-ttu-id="bdbc2-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bdbc2-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="bdbc2-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdbc2-141">NOTES</span></span>

## <span data-ttu-id="bdbc2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdbc2-142">RELATED LINKS</span></span>
