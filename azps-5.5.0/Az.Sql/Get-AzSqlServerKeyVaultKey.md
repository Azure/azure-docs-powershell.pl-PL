---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201498"
---
# <span data-ttu-id="ee1dc-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ee1dc-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ee1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1dc-103">Pobiera klucze magazynu kluczy serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="ee1dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee1dc-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1dc-106">Polecenie Get-AzSqlServerKeyVaultKey cmdlet pobiera informacje o kluczach magazynu kluczy na serwerze SQL.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="ee1dc-107">Możesz wyświetlić wszystkie klucze na serwerze lub wyświetlić określony klucz, podając klucz KeyId.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="ee1dc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee1dc-108">EXAMPLES</span></span>

### <span data-ttu-id="ee1dc-109">Przykład 1. Uzyskiwanie wszystkich kluczy magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="ee1dc-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ee1dc-110">To polecenie pobiera wszystkie klucze magazynu kluczy na serwerze SQL.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="ee1dc-111">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 112234455667788990011223344556677889900 CreationDate: 2017-01-01 12:00:00 ZasóbGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Typ: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 00998776655443322110099877665544332211 CreationDate: 2017-01-01 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ee1dc-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="ee1dc-112">Przykład 2. Uzyskiwanie określonego klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="ee1dc-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ee1dc-113">To polecenie pobiera klucz magazynu kluczy z identyfikatorem ', a następnie zapisuje go w $MyServerKeyVaultKey https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 zmienną.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="ee1dc-114">Możesz sprawdzić właściwości $MyServerKeyVaultKey, aby uzyskać szczegółowe informacje o magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="ee1dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1dc-115">PARAMETERS</span></span>

### <span data-ttu-id="ee1dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1dc-116">-DefaultProfile</span></span>
<span data-ttu-id="ee1dc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ee1dc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee1dc-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ee1dc-118">-KeyId</span></span>
<span data-ttu-id="ee1dc-119">Azure KeyId (Klucz klucza klucza platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="ee1dc-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1dc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1dc-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee1dc-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ee1dc-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ee1dc-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee1dc-122">-ServerName</span></span>
<span data-ttu-id="ee1dc-123">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-123">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1dc-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee1dc-124">-Confirm</span></span>
<span data-ttu-id="ee1dc-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1dc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1dc-126">-WhatIf</span></span>
<span data-ttu-id="ee1dc-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1dc-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1dc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1dc-129">CommonParameters</span></span>
<span data-ttu-id="ee1dc-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1dc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1dc-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1dc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1dc-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee1dc-132">INPUTS</span></span>

### <span data-ttu-id="ee1dc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee1dc-133">System.String</span></span>

## <span data-ttu-id="ee1dc-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee1dc-134">OUTPUTS</span></span>

### <span data-ttu-id="ee1dc-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ee1dc-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ee1dc-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee1dc-136">NOTES</span></span>

## <span data-ttu-id="ee1dc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee1dc-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee1dc-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ee1dc-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
