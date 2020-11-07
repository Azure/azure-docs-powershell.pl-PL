---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d2d2bd98491b5bf91aebb45e6b8a3368a58d1b56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707712"
---
# <span data-ttu-id="d7fbb-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d7fbb-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="d7fbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fbb-103">Ustawia funkcję ochrony przezroczystego szyfrowania danych (TDE) dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="d7fbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7fbb-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7fbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fbb-106">Polecenie cmdlet Set-AzSqlServerTransparentDataEncryptionProtector ustawia ochronę TDE dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="d7fbb-107">Zmiana typu funkcji ochrony TDE spowoduje obrócenie funkcji ochrony.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="d7fbb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7fbb-108">EXAMPLES</span></span>

### <span data-ttu-id="d7fbb-109">Przykład 1: Ustawianie przezroczystego typu szyfrowania danych (TDE) na servicemanage</span><span class="sxs-lookup"><span data-stu-id="d7fbb-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="d7fbb-110">To polecenie aktualizuje typ funkcji Ochrona TDE serwera na wartość zarządzana przez usługę.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="d7fbb-111">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="d7fbb-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="d7fbb-112">ContosoResourceGroup ContosoServer servicemanage</span><span class="sxs-lookup"><span data-stu-id="d7fbb-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="d7fbb-113">Przykład 2: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d7fbb-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="d7fbb-114">To polecenie aktualizuje serwer w celu użycia klucza magazynu kluczy serwera o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="d7fbb-115">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="d7fbb-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="d7fbb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="d7fbb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="d7fbb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7fbb-117">PARAMETERS</span></span>

### <span data-ttu-id="d7fbb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7fbb-118">-AsJob</span></span>
<span data-ttu-id="d7fbb-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7fbb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7fbb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fbb-120">-DefaultProfile</span></span>
<span data-ttu-id="d7fbb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7fbb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7fbb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d7fbb-122">-Force</span></span>
<span data-ttu-id="d7fbb-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="d7fbb-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7fbb-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d7fbb-124">-KeyId</span></span>
<span data-ttu-id="d7fbb-125">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7fbb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7fbb-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7fbb-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d7fbb-127">The name of the resource group</span></span>

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

### <span data-ttu-id="d7fbb-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d7fbb-128">-ServerName</span></span>
<span data-ttu-id="d7fbb-129">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d7fbb-130">-Type</span><span class="sxs-lookup"><span data-stu-id="d7fbb-130">-Type</span></span>
<span data-ttu-id="d7fbb-131">Typ funkcji Ochrona bazy danych usługi Azure Database TDE.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7fbb-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7fbb-132">-Confirm</span></span>
<span data-ttu-id="d7fbb-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7fbb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7fbb-134">-WhatIf</span></span>
<span data-ttu-id="d7fbb-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7fbb-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7fbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fbb-137">CommonParameters</span></span>
<span data-ttu-id="d7fbb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fbb-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7fbb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fbb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7fbb-140">INPUTS</span></span>

### <span data-ttu-id="d7fbb-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="d7fbb-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="d7fbb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d7fbb-142">System.String</span></span>

## <span data-ttu-id="d7fbb-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7fbb-143">OUTPUTS</span></span>

### <span data-ttu-id="d7fbb-144">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="d7fbb-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="d7fbb-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7fbb-145">NOTES</span></span>

## <span data-ttu-id="d7fbb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7fbb-146">RELATED LINKS</span></span>

[<span data-ttu-id="d7fbb-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d7fbb-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)