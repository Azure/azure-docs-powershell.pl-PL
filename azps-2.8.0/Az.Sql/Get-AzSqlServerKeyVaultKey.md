---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 6cc3b0f066f267b51a90c0cb0c56d1972ec92f5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887449"
---
# <span data-ttu-id="d6387-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6387-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="d6387-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6387-102">SYNOPSIS</span></span>
<span data-ttu-id="d6387-103">Pobiera klucze magazynu kluczy programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6387-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="d6387-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6387-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6387-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d6387-105">DESCRIPTION</span></span>
<span data-ttu-id="d6387-106">Polecenie cmdlet Get-AzSqlServerKeyVaultKey pobiera informacje o kluczach magazynu kluczy w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6387-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d6387-107">Możesz wyświetlić wszystkie klucze na serwerze lub wyświetlić określony klucz, dostarczając KeyId.</span><span class="sxs-lookup"><span data-stu-id="d6387-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="d6387-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6387-108">EXAMPLES</span></span>

### <span data-ttu-id="d6387-109">Przykład 1: pobieranie wszystkich kluczy magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d6387-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d6387-110">To polecenie pobiera wszystkie klucze magazynu kluczy na serwerze SQL.</span><span class="sxs-lookup"><span data-stu-id="d6387-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d6387-111">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 odcisk palca: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="d6387-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="d6387-112">Przykład 2: uzyskiwanie określonego klucza w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="d6387-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d6387-113">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ", a następnie zapisuje go w zmiennej $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="d6387-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="d6387-114">Możesz sprawdzić właściwości $MyServerKeyVaultKey, aby uzyskać szczegółowe informacje o magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6387-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="d6387-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6387-115">PARAMETERS</span></span>

### <span data-ttu-id="d6387-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6387-116">-DefaultProfile</span></span>
<span data-ttu-id="d6387-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d6387-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6387-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d6387-118">-KeyId</span></span>
<span data-ttu-id="d6387-119">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="d6387-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="d6387-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6387-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6387-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d6387-121">The name of the resource group</span></span>

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

### <span data-ttu-id="d6387-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d6387-122">-ServerName</span></span>
<span data-ttu-id="d6387-123">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6387-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d6387-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6387-124">-Confirm</span></span>
<span data-ttu-id="d6387-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6387-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6387-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6387-126">-WhatIf</span></span>
<span data-ttu-id="d6387-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6387-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6387-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6387-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6387-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6387-129">CommonParameters</span></span>
<span data-ttu-id="d6387-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6387-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6387-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6387-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6387-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6387-132">INPUTS</span></span>

### <span data-ttu-id="d6387-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d6387-133">System.String</span></span>

## <span data-ttu-id="d6387-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6387-134">OUTPUTS</span></span>

### <span data-ttu-id="d6387-135">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="d6387-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="d6387-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6387-136">NOTES</span></span>

## <span data-ttu-id="d6387-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6387-137">RELATED LINKS</span></span>

[<span data-ttu-id="d6387-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d6387-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
