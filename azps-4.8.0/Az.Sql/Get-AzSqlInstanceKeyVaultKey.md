---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222209"
---
# <span data-ttu-id="50e77-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="50e77-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="50e77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50e77-102">SYNOPSIS</span></span>
<span data-ttu-id="50e77-103">Pobiera klucze magazynu kluczy wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="50e77-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="50e77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50e77-104">SYNTAX</span></span>

### <span data-ttu-id="50e77-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="50e77-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e77-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e77-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e77-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e77-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e77-108">Opis</span><span class="sxs-lookup"><span data-stu-id="50e77-108">DESCRIPTION</span></span>
<span data-ttu-id="50e77-109">Polecenie cmdlet Get-AzSqlInstanceKeyVaultKey pobiera informacje o kluczach magazynu kluczy w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="50e77-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="50e77-110">Możesz wyświetlić wszystkie klucze w zarządzanym wystąpieniu lub wyświetlić określony klucz, dostarczając KeyId.</span><span class="sxs-lookup"><span data-stu-id="50e77-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="50e77-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50e77-111">EXAMPLES</span></span>

### <span data-ttu-id="50e77-112">Przykład 1: pobieranie wszystkich kluczy magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="50e77-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="50e77-113">To polecenie pobiera wszystkie klucze magazynu kluczy w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="50e77-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="50e77-114">Przykład 2: uzyskiwanie określonego klucza w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="50e77-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="50e77-115">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="50e77-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="50e77-116">Przykład 3: Używanie obiektu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="50e77-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="50e77-117">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="50e77-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="50e77-118">Przykład 4: korzystanie z identyfikatora zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="50e77-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="50e77-119">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="50e77-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="50e77-120">Przykład 5: korzystanie z połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="50e77-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="50e77-121">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="50e77-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="50e77-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50e77-122">PARAMETERS</span></span>

### <span data-ttu-id="50e77-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e77-123">-DefaultProfile</span></span>
<span data-ttu-id="50e77-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50e77-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50e77-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="50e77-125">-Instance</span></span>
<span data-ttu-id="50e77-126">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="50e77-126">The instance input object</span></span>

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

### <span data-ttu-id="50e77-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="50e77-127">-InstanceName</span></span>
<span data-ttu-id="50e77-128">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="50e77-128">The instance name</span></span>

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

### <span data-ttu-id="50e77-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="50e77-129">-InstanceResourceId</span></span>
<span data-ttu-id="50e77-130">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="50e77-130">The instance resource id</span></span>

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

### <span data-ttu-id="50e77-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="50e77-131">-KeyId</span></span>
<span data-ttu-id="50e77-132">Identyfikator klucza AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="50e77-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e77-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e77-133">-ResourceGroupName</span></span>
<span data-ttu-id="50e77-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="50e77-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="50e77-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50e77-135">-Confirm</span></span>
<span data-ttu-id="50e77-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50e77-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e77-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e77-137">-WhatIf</span></span>
<span data-ttu-id="50e77-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50e77-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50e77-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50e77-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50e77-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e77-140">CommonParameters</span></span>
<span data-ttu-id="50e77-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e77-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e77-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50e77-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e77-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50e77-143">INPUTS</span></span>

### <span data-ttu-id="50e77-144">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="50e77-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="50e77-145">System. String</span><span class="sxs-lookup"><span data-stu-id="50e77-145">System.String</span></span>

## <span data-ttu-id="50e77-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50e77-146">OUTPUTS</span></span>

### <span data-ttu-id="50e77-147">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="50e77-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="50e77-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50e77-148">NOTES</span></span>

## <span data-ttu-id="50e77-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50e77-149">RELATED LINKS</span></span>
