---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961473"
---
# <span data-ttu-id="2e1f9-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e1f9-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="2e1f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1f9-103">Dodaje klucz magazynu kluczy do serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="2e1f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2e1f9-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e1f9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2e1f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1f9-106">Polecenie Add-AzSqlServerKeyVaultKey cmdlet dodaje klucz magazynu kluczy do podanego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="2e1f9-107">Serwer musi mieć uprawnienia "get, wrapKey, unwrapKey" do magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="2e1f9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2e1f9-108">EXAMPLES</span></span>

### <span data-ttu-id="2e1f9-109">Przykład 1. Dodawanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="2e1f9-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="2e1f9-110">To polecenie dodaje klucz magazynu kluczy z identyfikatorem ' do serwera SQL o nazwie "ContosoServer" w grupie zasobów https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2e1f9-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="2e1f9-111">ResourceGroupName: ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122344566778899001123344556677889900 CreationDate: 2017-01-01 12:00:00</span><span class="sxs-lookup"><span data-stu-id="2e1f9-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="2e1f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e1f9-112">PARAMETERS</span></span>

### <span data-ttu-id="2e1f9-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2e1f9-113">-AsJob</span></span>
<span data-ttu-id="2e1f9-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2e1f9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e1f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1f9-115">-DefaultProfile</span></span>
<span data-ttu-id="2e1f9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2e1f9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e1f9-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2e1f9-117">-KeyId</span></span>
<span data-ttu-id="2e1f9-118">Azure KeyId (Klucz klucza klucza platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="2e1f9-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="2e1f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e1f9-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2e1f9-120">The name of the resource group</span></span>

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

### <span data-ttu-id="2e1f9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e1f9-121">-ServerName</span></span>
<span data-ttu-id="2e1f9-122">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2e1f9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e1f9-123">-Confirm</span></span>
<span data-ttu-id="2e1f9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e1f9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e1f9-125">-WhatIf</span></span>
<span data-ttu-id="2e1f9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e1f9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e1f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1f9-128">CommonParameters</span></span>
<span data-ttu-id="2e1f9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1f9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e1f9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1f9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e1f9-131">INPUTS</span></span>

### <span data-ttu-id="2e1f9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2e1f9-132">System.String</span></span>

## <span data-ttu-id="2e1f9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e1f9-133">OUTPUTS</span></span>

### <span data-ttu-id="2e1f9-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="2e1f9-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="2e1f9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2e1f9-135">NOTES</span></span>

## <span data-ttu-id="2e1f9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e1f9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e1f9-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2e1f9-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
