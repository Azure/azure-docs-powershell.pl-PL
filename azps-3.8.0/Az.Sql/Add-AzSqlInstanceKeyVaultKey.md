---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050236"
---
# <span data-ttu-id="14add-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="14add-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="14add-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14add-102">SYNOPSIS</span></span>
<span data-ttu-id="14add-103">Dodaje klucz magazynu kluczy do udostępnionego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="14add-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="14add-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14add-104">SYNTAX</span></span>

### <span data-ttu-id="14add-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14add-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14add-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14add-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14add-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14add-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14add-108">Opis</span><span class="sxs-lookup"><span data-stu-id="14add-108">DESCRIPTION</span></span>
<span data-ttu-id="14add-109">Polecenie cmdlet Add-AzSqlInstanceKeyVaultKey dodaje klucz magazynu kluczy do udostępnionego wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="14add-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="14add-110">W zarządzanym wystąpieniu muszą być przyznane uprawnienia Get, wrapKey, unwrapKey ', aby udzielić uprawnień do wystąpienia zarządzanego, należy użyć poniższego skryptu.</span><span class="sxs-lookup"><span data-stu-id="14add-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="14add-111">$managedInstance = Get-AzSqlInstance-Name "ContosoManagedInstanceName"-ResourceGroupName "ContosoResourceGroup" Set-AzKeyVaultAccessPolicy--ID-ObjectId $managedInstance. Identity. PrincipalId-PermissionsToKeys Get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="14add-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="14add-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14add-112">EXAMPLES</span></span>

### <span data-ttu-id="14add-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14add-113">Example 1</span></span>
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

<span data-ttu-id="14add-114">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do wystąpienia zarządzanego SQL o nazwie "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="14add-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="14add-115">Przykład 2: Używanie obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="14add-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="14add-116">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do wystąpienia zarządzanego SQL o nazwie "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="14add-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="14add-117">Przykład 3: używanie identyfikatora zasobu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="14add-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="14add-118">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do wystąpienia zarządzanego SQL o nazwie "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="14add-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="14add-119">Przykład 4: korzystanie z połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="14add-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="14add-120">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do wystąpienia zarządzanego SQL o nazwie "ContosoManagedInstanceName" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="14add-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="14add-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14add-121">PARAMETERS</span></span>

### <span data-ttu-id="14add-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14add-122">-DefaultProfile</span></span>
<span data-ttu-id="14add-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14add-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14add-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="14add-124">-Instance</span></span>
<span data-ttu-id="14add-125">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="14add-125">The instance input object</span></span>

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

### <span data-ttu-id="14add-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="14add-126">-InstanceName</span></span>
<span data-ttu-id="14add-127">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="14add-127">The instance name</span></span>

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

### <span data-ttu-id="14add-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="14add-128">-InstanceResourceId</span></span>
<span data-ttu-id="14add-129">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="14add-129">The instance resource id</span></span>

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

### <span data-ttu-id="14add-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="14add-130">-KeyId</span></span>
<span data-ttu-id="14add-131">Identyfikator klucza AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="14add-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="14add-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14add-132">-ResourceGroupName</span></span>
<span data-ttu-id="14add-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="14add-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="14add-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14add-134">-Confirm</span></span>
<span data-ttu-id="14add-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14add-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14add-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14add-136">-WhatIf</span></span>
<span data-ttu-id="14add-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14add-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14add-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14add-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14add-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14add-139">CommonParameters</span></span>
<span data-ttu-id="14add-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14add-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14add-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14add-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14add-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14add-142">INPUTS</span></span>

### <span data-ttu-id="14add-143">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="14add-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="14add-144">System. String</span><span class="sxs-lookup"><span data-stu-id="14add-144">System.String</span></span>

## <span data-ttu-id="14add-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14add-145">OUTPUTS</span></span>

### <span data-ttu-id="14add-146">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="14add-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="14add-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14add-147">NOTES</span></span>

## <span data-ttu-id="14add-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14add-148">RELATED LINKS</span></span>
