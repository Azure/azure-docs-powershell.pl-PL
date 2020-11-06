---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d78b6931e58469b20b2b937de083ff9d96f3f92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526530"
---
# <span data-ttu-id="4d5d9-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4d5d9-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="4d5d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d5d9-103">Ustawia funkcję ochrony przezroczystego szyfrowania danych (TDE) dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d5d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d5d9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d5d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="4d5d9-106">Polecenie cmdlet Set-AzureRmSqlServerTransparentDataEncryptionProtector ustawia ochronę TDE dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="4d5d9-107">Zmiana typu funkcji ochrony TDE spowoduje obrócenie funkcji ochrony.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="4d5d9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d5d9-108">EXAMPLES</span></span>

### <span data-ttu-id="4d5d9-109">Przykład 1: Ustawianie przezroczystego typu szyfrowania danych (TDE) na servicemanage</span><span class="sxs-lookup"><span data-stu-id="4d5d9-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4d5d9-110">To polecenie aktualizuje typ funkcji Ochrona TDE serwera na wartość zarządzana przez usługę.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="4d5d9-111">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4d5d9-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4d5d9-112">ContosoResourceGroup ContosoServer servicemanage</span><span class="sxs-lookup"><span data-stu-id="4d5d9-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="4d5d9-113">Przykład 2: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4d5d9-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4d5d9-114">To polecenie aktualizuje serwer w celu użycia klucza magazynu kluczy serwera o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="4d5d9-115">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4d5d9-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4d5d9-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="4d5d9-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="4d5d9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d5d9-117">PARAMETERS</span></span>

### <span data-ttu-id="4d5d9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d5d9-118">-AsJob</span></span>
<span data-ttu-id="4d5d9-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d5d9-119">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="4d5d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d5d9-120">-DefaultProfile</span></span>
<span data-ttu-id="4d5d9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d5d9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d5d9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4d5d9-122">-Force</span></span>
<span data-ttu-id="4d5d9-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="4d5d9-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4d5d9-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4d5d9-124">-KeyId</span></span>
<span data-ttu-id="4d5d9-125">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d5d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d5d9-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d5d9-127">The name of the resource group</span></span>

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

### <span data-ttu-id="4d5d9-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4d5d9-128">-ServerName</span></span>
<span data-ttu-id="4d5d9-129">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4d5d9-130">-Type</span><span class="sxs-lookup"><span data-stu-id="4d5d9-130">-Type</span></span>
<span data-ttu-id="4d5d9-131">Typ funkcji Ochrona bazy danych usługi Azure Database TDE.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d5d9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d5d9-132">-Confirm</span></span>
<span data-ttu-id="4d5d9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d5d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d5d9-134">-WhatIf</span></span>
<span data-ttu-id="4d5d9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d5d9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d5d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d5d9-137">CommonParameters</span></span>
<span data-ttu-id="4d5d9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d5d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d5d9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d5d9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d5d9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d5d9-140">INPUTS</span></span>

### <span data-ttu-id="4d5d9-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="4d5d9-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="4d5d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4d5d9-142">System.String</span></span>

## <span data-ttu-id="4d5d9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d5d9-143">OUTPUTS</span></span>

### <span data-ttu-id="4d5d9-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d5d9-144">System.Object</span></span>

## <span data-ttu-id="4d5d9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d5d9-145">NOTES</span></span>

## <span data-ttu-id="4d5d9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d5d9-146">RELATED LINKS</span></span>

[<span data-ttu-id="4d5d9-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4d5d9-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
