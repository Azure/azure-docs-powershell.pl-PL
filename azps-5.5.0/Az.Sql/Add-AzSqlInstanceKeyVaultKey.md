---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183394"
---
# <span data-ttu-id="fe4a1-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe4a1-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="fe4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4a1-103">Dodaje klucz magazynu klucza do podanego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="fe4a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe4a1-104">SYNTAX</span></span>

### <span data-ttu-id="fe4a1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fe4a1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe4a1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe4a1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe4a1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe4a1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe4a1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe4a1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe4a1-109">Polecenie Add-AzSqlInstanceKeyVaultKey cmdlet dodaje klucz magazynu klucza do podanego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="fe4a1-110">Zarządzane wystąpienie musi mieć uprawnienia "get, wrapKey, unwrapKey" do magazynu, użyć poniższego skryptu, aby udzielić uprawnień do zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="fe4a1-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="fe4a1-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="fe4a1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe4a1-112">EXAMPLES</span></span>

### <span data-ttu-id="fe4a1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe4a1-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="fe4a1-114">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe4a1-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="fe4a1-115">Przykład 2. Używanie obiektu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="fe4a1-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="fe4a1-116">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe4a1-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="fe4a1-117">Przykład 3. Używanie identyfikatora zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="fe4a1-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="fe4a1-118">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe4a1-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="fe4a1-119">Przykład 4. Używanie rur</span><span class="sxs-lookup"><span data-stu-id="fe4a1-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="fe4a1-120">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe4a1-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="fe4a1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe4a1-121">PARAMETERS</span></span>

### <span data-ttu-id="fe4a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4a1-122">-DefaultProfile</span></span>
<span data-ttu-id="fe4a1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe4a1-124">—Instance</span><span class="sxs-lookup"><span data-stu-id="fe4a1-124">-Instance</span></span>
<span data-ttu-id="fe4a1-125">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="fe4a1-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a1-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fe4a1-126">-InstanceName</span></span>
<span data-ttu-id="fe4a1-127">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="fe4a1-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a1-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="fe4a1-128">-InstanceResourceId</span></span>
<span data-ttu-id="fe4a1-129">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="fe4a1-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a1-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="fe4a1-130">-KeyId</span></span>
<span data-ttu-id="fe4a1-131">Identyfikator klucza usługi AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe4a1-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4a1-132">-ResourceGroupName</span></span>
<span data-ttu-id="fe4a1-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fe4a1-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a1-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe4a1-134">-Confirm</span></span>
<span data-ttu-id="fe4a1-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe4a1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4a1-136">-WhatIf</span></span>
<span data-ttu-id="fe4a1-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4a1-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe4a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4a1-139">CommonParameters</span></span>
<span data-ttu-id="fe4a1-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4a1-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe4a1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4a1-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe4a1-142">INPUTS</span></span>

### <span data-ttu-id="fe4a1-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fe4a1-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="fe4a1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fe4a1-144">System.String</span></span>

## <span data-ttu-id="fe4a1-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe4a1-145">OUTPUTS</span></span>

### <span data-ttu-id="fe4a1-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="fe4a1-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="fe4a1-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe4a1-147">NOTES</span></span>

## <span data-ttu-id="fe4a1-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe4a1-148">RELATED LINKS</span></span>
