---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334942"
---
# <span data-ttu-id="84237-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="84237-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84237-102">SYNOPSIS</span></span>
<span data-ttu-id="84237-103">Zaktualizuj stan modułu HSM zarządzanego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="84237-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="84237-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84237-104">SYNTAX</span></span>

### <span data-ttu-id="84237-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84237-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84237-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84237-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84237-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84237-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84237-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84237-108">DESCRIPTION</span></span>
<span data-ttu-id="84237-109">To polecenie cmdlet aktualizuje stan modułu HSM zarządzanego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="84237-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="84237-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84237-110">EXAMPLES</span></span>

### <span data-ttu-id="84237-111">Przykład 1: aktualizowanie zarządzanego modułu HSM bezpośrednio</span><span class="sxs-lookup"><span data-stu-id="84237-111">Example 1: Update a managed Hsm directly</span></span>
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

<span data-ttu-id="84237-112">Aktualizuje znaczniki zarządzanego modułu HSM o nazwie `$hsmName` w grupie zasobów `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="84237-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="84237-113">Przykład 2: aktualizowanie zarządzanego modułu HSM za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="84237-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="84237-114">Aktualizuje znaczniki zarządzanego modułu HSM za pomocą składni połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="84237-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="84237-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84237-115">PARAMETERS</span></span>

### <span data-ttu-id="84237-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84237-116">-DefaultProfile</span></span>
<span data-ttu-id="84237-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84237-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84237-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84237-118">-InputObject</span></span>
<span data-ttu-id="84237-119">Zarządzany obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="84237-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="84237-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84237-120">-Name</span></span>
<span data-ttu-id="84237-121">Nazwa zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="84237-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="84237-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84237-122">-ResourceGroupName</span></span>
<span data-ttu-id="84237-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84237-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="84237-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84237-124">-ResourceId</span></span>
<span data-ttu-id="84237-125">Identyfikator zasobu zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="84237-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="84237-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="84237-126">-Tag</span></span>
<span data-ttu-id="84237-127">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="84237-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="84237-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84237-128">-Confirm</span></span>
<span data-ttu-id="84237-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84237-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84237-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84237-130">-WhatIf</span></span>
<span data-ttu-id="84237-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84237-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84237-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84237-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84237-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84237-133">CommonParameters</span></span>
<span data-ttu-id="84237-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84237-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84237-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84237-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84237-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84237-136">INPUTS</span></span>

### <span data-ttu-id="84237-137">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="84237-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84237-138">System.String</span></span>

### <span data-ttu-id="84237-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84237-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84237-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84237-140">OUTPUTS</span></span>

### <span data-ttu-id="84237-141">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="84237-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84237-142">NOTES</span></span>

## <span data-ttu-id="84237-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84237-143">RELATED LINKS</span></span>

[<span data-ttu-id="84237-144">Nowe — AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="84237-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="84237-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="84237-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)