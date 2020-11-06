---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 4f26955db9d99871cb0c5ae127b5977deedacf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524838"
---
# <span data-ttu-id="b4866-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b4866-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="b4866-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4866-102">SYNOPSIS</span></span>
<span data-ttu-id="b4866-103">Pobiera klucze magazynu kluczy programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b4866-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4866-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4866-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4866-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4866-105">DESCRIPTION</span></span>
<span data-ttu-id="b4866-106">Polecenie cmdlet Get-AzureRmSqlServerKeyVaultKey pobiera informacje o kluczach magazynu kluczy w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b4866-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="b4866-107">Możesz wyświetlić wszystkie klucze na serwerze lub wyświetlić określony klucz, dostarczając KeyId.</span><span class="sxs-lookup"><span data-stu-id="b4866-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="b4866-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4866-108">EXAMPLES</span></span>

### <span data-ttu-id="b4866-109">Przykład 1: pobieranie wszystkich kluczy magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b4866-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b4866-110">To polecenie pobiera wszystkie klucze magazynu kluczy na serwerze SQL.</span><span class="sxs-lookup"><span data-stu-id="b4866-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="b4866-111">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="b4866-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="b4866-112">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 odcisk palca: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="b4866-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="b4866-113">Przykład 2: uzyskiwanie określonego klucza w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="b4866-113">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b4866-114">To polecenie pobiera klucz magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ", a następnie zapisuje go w zmiennej $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="b4866-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="b4866-115">Możesz sprawdzić właściwości $MyServerKeyVaultKey, aby uzyskać szczegółowe informacje o magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b4866-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="b4866-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4866-116">PARAMETERS</span></span>

### <span data-ttu-id="b4866-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4866-117">-DefaultProfile</span></span>
<span data-ttu-id="b4866-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b4866-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-119">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b4866-119">-KeyId</span></span>
<span data-ttu-id="b4866-120">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="b4866-120">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4866-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4866-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4866-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b4866-123">-ServerName</span></span>
<span data-ttu-id="b4866-124">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b4866-124">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4866-125">-Confirm</span></span>
<span data-ttu-id="b4866-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4866-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4866-127">-WhatIf</span></span>
<span data-ttu-id="b4866-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4866-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4866-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4866-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4866-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4866-130">CommonParameters</span></span>
<span data-ttu-id="b4866-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4866-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4866-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4866-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4866-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4866-133">INPUTS</span></span>

### <span data-ttu-id="b4866-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4866-134">System.String</span></span>

## <span data-ttu-id="b4866-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4866-135">OUTPUTS</span></span>

### <span data-ttu-id="b4866-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="b4866-136">System.Object</span></span>

## <span data-ttu-id="b4866-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4866-137">NOTES</span></span>

## <span data-ttu-id="b4866-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4866-138">RELATED LINKS</span></span>

[<span data-ttu-id="b4866-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b4866-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
