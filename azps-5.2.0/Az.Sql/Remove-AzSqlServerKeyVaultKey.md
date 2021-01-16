---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322691"
---
# <span data-ttu-id="4b302-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4b302-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="4b302-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b302-102">SYNOPSIS</span></span>
<span data-ttu-id="4b302-103">Usuwa klucz magazynu kluczy z programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4b302-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="4b302-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b302-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b302-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b302-105">DESCRIPTION</span></span>
<span data-ttu-id="4b302-106">Polecenie cmdlet Remove-AzSqlServerKeyVaultKey usuwa klucz magazynu kluczy z określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="4b302-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="4b302-107">Zauważ, że uprawnienia programu SQL Server do magazynu kluczy nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="4b302-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="4b302-108">Aby zmienić uprawnienia, użyj ustawienia Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="4b302-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="4b302-109">Pamiętaj, że to polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="4b302-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="4b302-110">Aby usunąć klucz z magazynu kluczy, użyj przycisku Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="4b302-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="4b302-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b302-111">EXAMPLES</span></span>

### <span data-ttu-id="4b302-112">Przykład 1: Usuwanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="4b302-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="4b302-113">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="4b302-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="4b302-114">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="4b302-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="4b302-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b302-115">PARAMETERS</span></span>

### <span data-ttu-id="4b302-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b302-116">-AsJob</span></span>
<span data-ttu-id="4b302-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4b302-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b302-118">-DefaultProfile</span></span>
<span data-ttu-id="4b302-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4b302-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b302-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4b302-120">-KeyId</span></span>
<span data-ttu-id="4b302-121">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="4b302-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="4b302-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b302-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b302-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4b302-123">The name of the resource group</span></span>

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

### <span data-ttu-id="4b302-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4b302-124">-ServerName</span></span>
<span data-ttu-id="4b302-125">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4b302-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4b302-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b302-126">-Confirm</span></span>
<span data-ttu-id="4b302-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b302-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b302-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b302-128">-WhatIf</span></span>
<span data-ttu-id="4b302-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b302-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b302-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b302-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b302-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b302-131">CommonParameters</span></span>
<span data-ttu-id="4b302-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b302-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b302-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b302-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b302-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b302-134">INPUTS</span></span>

### <span data-ttu-id="4b302-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4b302-135">System.String</span></span>

## <span data-ttu-id="4b302-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b302-136">OUTPUTS</span></span>

### <span data-ttu-id="4b302-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="4b302-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="4b302-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b302-138">NOTES</span></span>

## <span data-ttu-id="4b302-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b302-139">RELATED LINKS</span></span>

[<span data-ttu-id="4b302-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4b302-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
