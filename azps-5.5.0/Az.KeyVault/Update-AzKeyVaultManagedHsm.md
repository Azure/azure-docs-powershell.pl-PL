---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185386"
---
# <span data-ttu-id="9b225-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="9b225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b225-102">SYNOPSIS</span></span>
<span data-ttu-id="9b225-103">Aktualizowanie stanu zarządzanego systemu Azure HSM.</span><span class="sxs-lookup"><span data-stu-id="9b225-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="9b225-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b225-104">SYNTAX</span></span>

### <span data-ttu-id="9b225-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9b225-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b225-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b225-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b225-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b225-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b225-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b225-108">DESCRIPTION</span></span>
<span data-ttu-id="9b225-109">To polecenie cmdlet aktualizuje stan zarządzanego modułu HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b225-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="9b225-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b225-110">EXAMPLES</span></span>

### <span data-ttu-id="9b225-111">Przykład 1. Bezpośrednia aktualizacja zarządzanego obiektu Hsm</span><span class="sxs-lookup"><span data-stu-id="9b225-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="9b225-112">Aktualizacje tagów zarządzanego modułu Hsm `$hsmName` nazwanych w grupie `$resourceGroupName` zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b225-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="9b225-113">Przykład 2. Aktualizowanie zarządzanego hsm za pomocą linii rurowych</span><span class="sxs-lookup"><span data-stu-id="9b225-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="9b225-114">Aktualizuje tagi zarządzanego hsm przy użyciu składni linii rurowych.</span><span class="sxs-lookup"><span data-stu-id="9b225-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="9b225-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b225-115">PARAMETERS</span></span>

### <span data-ttu-id="9b225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b225-116">-DefaultProfile</span></span>
<span data-ttu-id="9b225-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b225-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b225-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b225-118">-InputObject</span></span>
<span data-ttu-id="9b225-119">Zarządzany obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="9b225-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b225-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b225-120">-Name</span></span>
<span data-ttu-id="9b225-121">Nazwa zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="9b225-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b225-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b225-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b225-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b225-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b225-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b225-124">-ResourceId</span></span>
<span data-ttu-id="9b225-125">Identyfikator zasobu zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="9b225-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b225-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="9b225-126">-Tag</span></span>
<span data-ttu-id="9b225-127">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b225-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b225-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b225-128">-Confirm</span></span>
<span data-ttu-id="9b225-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b225-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b225-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b225-130">-WhatIf</span></span>
<span data-ttu-id="9b225-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b225-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b225-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b225-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b225-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b225-133">CommonParameters</span></span>
<span data-ttu-id="9b225-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b225-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b225-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b225-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b225-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b225-136">INPUTS</span></span>

### <span data-ttu-id="9b225-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="9b225-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9b225-138">System.String</span></span>

### <span data-ttu-id="9b225-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b225-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b225-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b225-140">OUTPUTS</span></span>

### <span data-ttu-id="9b225-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="9b225-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b225-142">NOTES</span></span>

## <span data-ttu-id="9b225-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b225-143">RELATED LINKS</span></span>

[<span data-ttu-id="9b225-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="9b225-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="9b225-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9b225-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)