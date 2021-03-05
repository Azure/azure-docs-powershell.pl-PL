---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 5a83d442f0b12731de3a00468283a8539b529fa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961521"
---
# <span data-ttu-id="d838f-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d838f-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="d838f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d838f-102">SYNOPSIS</span></span>
<span data-ttu-id="d838f-103">Dodaje klucz magazynu klucza do podanego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d838f-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="d838f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d838f-104">SYNTAX</span></span>

### <span data-ttu-id="d838f-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d838f-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d838f-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d838f-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d838f-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d838f-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d838f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d838f-108">DESCRIPTION</span></span>
<span data-ttu-id="d838f-109">Polecenie Add-AzSqlInstanceKeyVaultKey cmdlet dodaje klucz magazynu klucza do podanego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d838f-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="d838f-110">Zarządzane wystąpienie musi mieć uprawnienia "get, wrapKey, unwrapKey" do magazynu, użyj poniższego skryptu, aby udzielić uprawnień do zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d838f-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="d838f-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="d838f-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="d838f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d838f-112">EXAMPLES</span></span>

### <span data-ttu-id="d838f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d838f-113">Example 1</span></span>
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

<span data-ttu-id="d838f-114">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d838f-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="d838f-115">Przykład 2. Używanie obiektu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d838f-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="d838f-116">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d838f-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="d838f-117">Przykład 3. Używanie identyfikatora zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d838f-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="d838f-118">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d838f-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="d838f-119">Przykład 4. Stosowanie rur</span><span class="sxs-lookup"><span data-stu-id="d838f-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="d838f-120">To polecenie dodaje klucz magazynu kluczy o identyfikatorze ' do wystąpienia zarządzanego przez język SQL o nazwie https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d838f-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="d838f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d838f-121">PARAMETERS</span></span>

### <span data-ttu-id="d838f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d838f-122">-DefaultProfile</span></span>
<span data-ttu-id="d838f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d838f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d838f-124">—Instance</span><span class="sxs-lookup"><span data-stu-id="d838f-124">-Instance</span></span>
<span data-ttu-id="d838f-125">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d838f-125">The instance input object</span></span>

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

### <span data-ttu-id="d838f-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d838f-126">-InstanceName</span></span>
<span data-ttu-id="d838f-127">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d838f-127">The instance name</span></span>

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

### <span data-ttu-id="d838f-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d838f-128">-InstanceResourceId</span></span>
<span data-ttu-id="d838f-129">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="d838f-129">The instance resource id</span></span>

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

### <span data-ttu-id="d838f-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d838f-130">-KeyId</span></span>
<span data-ttu-id="d838f-131">Identyfikator klucza usługi AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="d838f-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="d838f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d838f-132">-ResourceGroupName</span></span>
<span data-ttu-id="d838f-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d838f-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="d838f-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d838f-134">-Confirm</span></span>
<span data-ttu-id="d838f-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d838f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d838f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d838f-136">-WhatIf</span></span>
<span data-ttu-id="d838f-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d838f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d838f-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d838f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d838f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d838f-139">CommonParameters</span></span>
<span data-ttu-id="d838f-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d838f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d838f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d838f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d838f-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d838f-142">INPUTS</span></span>

### <span data-ttu-id="d838f-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d838f-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="d838f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d838f-144">System.String</span></span>

## <span data-ttu-id="d838f-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d838f-145">OUTPUTS</span></span>

### <span data-ttu-id="d838f-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="d838f-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="d838f-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d838f-147">NOTES</span></span>

## <span data-ttu-id="d838f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d838f-148">RELATED LINKS</span></span>
