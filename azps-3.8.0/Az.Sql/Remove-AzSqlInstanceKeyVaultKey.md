---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051912"
---
# <span data-ttu-id="1338b-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1338b-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="1338b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1338b-102">SYNOPSIS</span></span>
<span data-ttu-id="1338b-103">Usuwa klucz magazynu kluczy z wystąpienia zarządzanego przez SQL</span><span class="sxs-lookup"><span data-stu-id="1338b-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="1338b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1338b-104">SYNTAX</span></span>

### <span data-ttu-id="1338b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1338b-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1338b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1338b-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1338b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1338b-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1338b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1338b-108">DESCRIPTION</span></span>
<span data-ttu-id="1338b-109">Polecenie cmdlet Remove-AzSqlInstanceKeyVaultKey usuwa klucz magazynu kluczy z określonego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1338b-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="1338b-110">Pamiętaj, że uprawnienia wystąpienia zarządzanego przez SQL do magazynu kluczy nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="1338b-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="1338b-111">Aby zmienić uprawnienia, użyj ustawienia Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="1338b-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="1338b-112">Pamiętaj, że to polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1338b-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="1338b-113">Aby usunąć klucz z magazynu kluczy, użyj przycisku Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="1338b-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="1338b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1338b-114">EXAMPLES</span></span>

### <span data-ttu-id="1338b-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1338b-115">Example 1</span></span>
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

<span data-ttu-id="1338b-116">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1338b-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="1338b-117">Przykład 2: Używanie obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="1338b-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="1338b-118">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1338b-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="1338b-119">Przykład 3: używanie identyfikatora zasobu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="1338b-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="1338b-120">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1338b-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="1338b-121">Przykład 4: korzystanie z połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="1338b-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="1338b-122">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 z określonego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="1338b-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="1338b-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1338b-123">PARAMETERS</span></span>

### <span data-ttu-id="1338b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1338b-124">-DefaultProfile</span></span>
<span data-ttu-id="1338b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1338b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1338b-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="1338b-126">-Instance</span></span>
<span data-ttu-id="1338b-127">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1338b-127">The instance input object</span></span>

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

### <span data-ttu-id="1338b-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1338b-128">-InstanceName</span></span>
<span data-ttu-id="1338b-129">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1338b-129">The instance name</span></span>

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

### <span data-ttu-id="1338b-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="1338b-130">-InstanceResourceId</span></span>
<span data-ttu-id="1338b-131">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="1338b-131">The instance resource id</span></span>

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

### <span data-ttu-id="1338b-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="1338b-132">-KeyId</span></span>
<span data-ttu-id="1338b-133">Identyfikator klucza AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="1338b-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="1338b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1338b-134">-ResourceGroupName</span></span>
<span data-ttu-id="1338b-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1338b-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="1338b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1338b-136">-Confirm</span></span>
<span data-ttu-id="1338b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1338b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1338b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1338b-138">-WhatIf</span></span>
<span data-ttu-id="1338b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1338b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1338b-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1338b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1338b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1338b-141">CommonParameters</span></span>
<span data-ttu-id="1338b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1338b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1338b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1338b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1338b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1338b-144">INPUTS</span></span>

### <span data-ttu-id="1338b-145">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1338b-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="1338b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1338b-146">System.String</span></span>

## <span data-ttu-id="1338b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1338b-147">OUTPUTS</span></span>

### <span data-ttu-id="1338b-148">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="1338b-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="1338b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1338b-149">NOTES</span></span>

## <span data-ttu-id="1338b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1338b-150">RELATED LINKS</span></span>
