---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197651"
---
# <span data-ttu-id="0e90b-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e90b-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="0e90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e90b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e90b-103">Usuwa klucz magazynu kluczy z serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="0e90b-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="0e90b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e90b-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e90b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e90b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e90b-106">Polecenie Remove-AzSqlServerKeyVaultKey cmdlet usuwa klucz magazynu kluczy z określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="0e90b-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="0e90b-107">Uprawnienia serwera SQL do magazynu klucza nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="0e90b-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="0e90b-108">Aby zmienić uprawnienia, użyj ustawienia Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="0e90b-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="0e90b-109">To polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0e90b-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="0e90b-110">Aby usunąć klucz z magazynu kluczy, użyj klawisza Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="0e90b-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="0e90b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e90b-111">EXAMPLES</span></span>

### <span data-ttu-id="0e90b-112">Przykład 1. Usuwanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="0e90b-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="0e90b-113">To polecenie usuwa z określonego serwera klucz magazynu kluczy o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorze '.</span><span class="sxs-lookup"><span data-stu-id="0e90b-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="0e90b-114">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344566778899001123344556677889900 CreationDate: 2017-01-01 12:00:00</span><span class="sxs-lookup"><span data-stu-id="0e90b-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="0e90b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e90b-115">PARAMETERS</span></span>

### <span data-ttu-id="0e90b-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0e90b-116">-AsJob</span></span>
<span data-ttu-id="0e90b-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0e90b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e90b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e90b-118">-DefaultProfile</span></span>
<span data-ttu-id="0e90b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0e90b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e90b-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="0e90b-120">-KeyId</span></span>
<span data-ttu-id="0e90b-121">Azure KeyId (Klucz klucza klucza platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="0e90b-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e90b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e90b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e90b-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e90b-123">The name of the resource group</span></span>

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

### <span data-ttu-id="0e90b-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e90b-124">-ServerName</span></span>
<span data-ttu-id="0e90b-125">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="0e90b-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0e90b-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e90b-126">-Confirm</span></span>
<span data-ttu-id="0e90b-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e90b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e90b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e90b-128">-WhatIf</span></span>
<span data-ttu-id="0e90b-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e90b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e90b-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e90b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e90b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e90b-131">CommonParameters</span></span>
<span data-ttu-id="0e90b-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e90b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e90b-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e90b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e90b-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e90b-134">INPUTS</span></span>

### <span data-ttu-id="0e90b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0e90b-135">System.String</span></span>

## <span data-ttu-id="0e90b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e90b-136">OUTPUTS</span></span>

### <span data-ttu-id="0e90b-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="0e90b-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="0e90b-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e90b-138">NOTES</span></span>

## <span data-ttu-id="0e90b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e90b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e90b-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0e90b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
