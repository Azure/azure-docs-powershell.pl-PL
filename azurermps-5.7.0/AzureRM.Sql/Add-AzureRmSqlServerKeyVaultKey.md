---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: bf82ca7804ecd3f382728217395be234155e9035
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544088"
---
# <span data-ttu-id="b6306-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b6306-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="b6306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6306-102">SYNOPSIS</span></span>
<span data-ttu-id="b6306-103">Dodaje klucz magazynu kluczy do programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b6306-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6306-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6306-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6306-105">DESCRIPTION</span></span>
<span data-ttu-id="b6306-106">Polecenie cmdlet Add-AzureRmSqlServerKeyVaultKey dodaje klucz magazynu kluczy do dostarczonego programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b6306-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="b6306-107">Serwer musi mieć uprawnienia Get, wrapKey, unwrapKey ' do magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6306-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="b6306-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6306-108">EXAMPLES</span></span>

### <span data-ttu-id="b6306-109">Przykład 1: Dodawanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b6306-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b6306-110">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do programu SQL Server o nazwie "ContosoServer" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="b6306-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="b6306-111">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="b6306-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="b6306-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6306-112">PARAMETERS</span></span>

### <span data-ttu-id="b6306-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6306-113">-AsJob</span></span>
<span data-ttu-id="b6306-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b6306-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6306-115">-DefaultProfile</span></span>
<span data-ttu-id="b6306-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6306-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6306-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b6306-117">-KeyId</span></span>
<span data-ttu-id="b6306-118">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="b6306-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6306-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6306-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6306-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b6306-120">The name of the resource group</span></span>

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

### <span data-ttu-id="b6306-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b6306-121">-ServerName</span></span>
<span data-ttu-id="b6306-122">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b6306-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b6306-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6306-123">-Confirm</span></span>
<span data-ttu-id="b6306-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6306-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6306-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6306-125">-WhatIf</span></span>
<span data-ttu-id="b6306-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6306-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6306-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6306-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6306-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6306-128">CommonParameters</span></span>
<span data-ttu-id="b6306-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6306-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6306-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6306-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6306-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6306-131">INPUTS</span></span>

### <span data-ttu-id="b6306-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b6306-132">System.String</span></span>

## <span data-ttu-id="b6306-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6306-133">OUTPUTS</span></span>

### <span data-ttu-id="b6306-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="b6306-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="b6306-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6306-135">NOTES</span></span>

## <span data-ttu-id="b6306-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6306-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6306-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b6306-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
