---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176819"
---
# <span data-ttu-id="95731-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95731-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="95731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95731-102">SYNOPSIS</span></span>
<span data-ttu-id="95731-103">Usuwa klucz magazynu kluczy z wystąpienia zarządzanego przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="95731-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="95731-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95731-104">SYNTAX</span></span>

### <span data-ttu-id="95731-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="95731-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95731-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95731-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95731-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95731-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95731-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="95731-108">DESCRIPTION</span></span>
<span data-ttu-id="95731-109">To Remove-AzSqlInstanceKeyVaultKey cmdlet usuwa klucz magazynu kluczy z określonego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="95731-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="95731-110">Zwróć uwagę, że uprawnienia wystąpienia zarządzanego przez sql do magazynu klucza nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="95731-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="95731-111">Aby zmienić uprawnienia, użyj ustawienia Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="95731-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="95731-112">To polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="95731-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="95731-113">Aby usunąć klucz z magazynu kluczy, użyj klawisza Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="95731-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="95731-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95731-114">EXAMPLES</span></span>

### <span data-ttu-id="95731-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95731-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="95731-116">To polecenie usuwa klucz magazynu kluczy o identyfikatorze ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="95731-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="95731-117">Przykład 2. Używanie obiektu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="95731-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="95731-118">To polecenie usuwa klucz magazynu kluczy o identyfikatorze ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="95731-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="95731-119">Przykład 3. Używanie identyfikatora zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="95731-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="95731-120">To polecenie usuwa klucz magazynu kluczy o identyfikatorze ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="95731-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="95731-121">Przykład 4. Używanie rur</span><span class="sxs-lookup"><span data-stu-id="95731-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="95731-122">To polecenie usuwa klucz magazynu kluczy o identyfikatorze ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="95731-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="95731-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95731-123">PARAMETERS</span></span>

### <span data-ttu-id="95731-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95731-124">-DefaultProfile</span></span>
<span data-ttu-id="95731-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95731-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95731-126">—Instance</span><span class="sxs-lookup"><span data-stu-id="95731-126">-Instance</span></span>
<span data-ttu-id="95731-127">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="95731-127">The instance input object</span></span>

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

### <span data-ttu-id="95731-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="95731-128">-InstanceName</span></span>
<span data-ttu-id="95731-129">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="95731-129">The instance name</span></span>

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

### <span data-ttu-id="95731-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="95731-130">-InstanceResourceId</span></span>
<span data-ttu-id="95731-131">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="95731-131">The instance resource id</span></span>

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

### <span data-ttu-id="95731-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="95731-132">-KeyId</span></span>
<span data-ttu-id="95731-133">Identyfikator klucza usługi AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="95731-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="95731-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95731-134">-ResourceGroupName</span></span>
<span data-ttu-id="95731-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="95731-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="95731-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95731-136">-Confirm</span></span>
<span data-ttu-id="95731-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95731-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95731-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95731-138">-WhatIf</span></span>
<span data-ttu-id="95731-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95731-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95731-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95731-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95731-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95731-141">CommonParameters</span></span>
<span data-ttu-id="95731-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95731-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95731-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95731-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95731-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95731-144">INPUTS</span></span>

### <span data-ttu-id="95731-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="95731-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="95731-146">System.String</span><span class="sxs-lookup"><span data-stu-id="95731-146">System.String</span></span>

## <span data-ttu-id="95731-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95731-147">OUTPUTS</span></span>

### <span data-ttu-id="95731-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="95731-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="95731-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95731-149">NOTES</span></span>

## <span data-ttu-id="95731-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95731-150">RELATED LINKS</span></span>
