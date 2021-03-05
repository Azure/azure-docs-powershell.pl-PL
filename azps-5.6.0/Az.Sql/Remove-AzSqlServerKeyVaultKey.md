---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967345"
---
# <span data-ttu-id="631f1-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="631f1-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="631f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631f1-102">SYNOPSIS</span></span>
<span data-ttu-id="631f1-103">Usuwa klucz magazynu kluczy z serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="631f1-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="631f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="631f1-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631f1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="631f1-105">DESCRIPTION</span></span>
<span data-ttu-id="631f1-106">Polecenie Remove-AzSqlServerKeyVaultKey cmdlet usuwa klucz magazynu kluczy z określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="631f1-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="631f1-107">Uprawnienia serwera SQL do magazynu klucza nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="631f1-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="631f1-108">Aby zmienić uprawnienia, użyj ustawienia Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="631f1-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="631f1-109">To polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="631f1-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="631f1-110">Aby usunąć klucz z magazynu kluczy, użyj klawisza Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="631f1-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="631f1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="631f1-111">EXAMPLES</span></span>

### <span data-ttu-id="631f1-112">Przykład 1. Usuwanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="631f1-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="631f1-113">To polecenie usuwa z określonego serwera klucz magazynu kluczy o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorze '.</span><span class="sxs-lookup"><span data-stu-id="631f1-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="631f1-114">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344566778899001123344556677889900 CreationDate: 2017-01-01 12:00:00</span><span class="sxs-lookup"><span data-stu-id="631f1-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="631f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631f1-115">PARAMETERS</span></span>

### <span data-ttu-id="631f1-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="631f1-116">-AsJob</span></span>
<span data-ttu-id="631f1-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="631f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="631f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631f1-118">-DefaultProfile</span></span>
<span data-ttu-id="631f1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="631f1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="631f1-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="631f1-120">-KeyId</span></span>
<span data-ttu-id="631f1-121">Azure KeyId (Klucz klucza klucza platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="631f1-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="631f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="631f1-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="631f1-123">The name of the resource group</span></span>

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

### <span data-ttu-id="631f1-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="631f1-124">-ServerName</span></span>
<span data-ttu-id="631f1-125">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="631f1-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="631f1-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="631f1-126">-Confirm</span></span>
<span data-ttu-id="631f1-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="631f1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631f1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631f1-128">-WhatIf</span></span>
<span data-ttu-id="631f1-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="631f1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631f1-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="631f1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631f1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631f1-131">CommonParameters</span></span>
<span data-ttu-id="631f1-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631f1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631f1-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631f1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631f1-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="631f1-134">INPUTS</span></span>

### <span data-ttu-id="631f1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="631f1-135">System.String</span></span>

## <span data-ttu-id="631f1-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="631f1-136">OUTPUTS</span></span>

### <span data-ttu-id="631f1-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="631f1-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="631f1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="631f1-138">NOTES</span></span>

## <span data-ttu-id="631f1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="631f1-139">RELATED LINKS</span></span>

[<span data-ttu-id="631f1-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="631f1-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
