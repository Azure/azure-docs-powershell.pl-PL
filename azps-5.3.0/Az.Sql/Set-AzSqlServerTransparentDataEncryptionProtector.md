---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489445"
---
# <span data-ttu-id="484ac-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="484ac-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="484ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="484ac-102">SYNOPSIS</span></span>
<span data-ttu-id="484ac-103">Ustawia funkcję ochrony przezroczystego szyfrowania danych (TDE) dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="484ac-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="484ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="484ac-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="484ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="484ac-105">DESCRIPTION</span></span>
<span data-ttu-id="484ac-106">Polecenie cmdlet Set-AzSqlServerTransparentDataEncryptionProtector ustawia ochronę TDE dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="484ac-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="484ac-107">Zmiana typu funkcji ochrony TDE spowoduje obrócenie funkcji ochrony.</span><span class="sxs-lookup"><span data-stu-id="484ac-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="484ac-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="484ac-108">EXAMPLES</span></span>

### <span data-ttu-id="484ac-109">Przykład 1: Ustawianie przezroczystego typu szyfrowania danych (TDE) na servicemanage</span><span class="sxs-lookup"><span data-stu-id="484ac-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="484ac-110">To polecenie aktualizuje typ funkcji Ochrona TDE serwera na wartość zarządzana przez usługę.</span><span class="sxs-lookup"><span data-stu-id="484ac-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="484ac-111">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="484ac-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="484ac-112">ContosoResourceGroup ContosoServer servicemanage</span><span class="sxs-lookup"><span data-stu-id="484ac-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="484ac-113">Przykład 2: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="484ac-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="484ac-114">To polecenie aktualizuje serwer w celu użycia klucza magazynu kluczy serwera o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="484ac-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="484ac-115">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="484ac-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="484ac-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="484ac-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="484ac-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="484ac-117">PARAMETERS</span></span>

### <span data-ttu-id="484ac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="484ac-118">-AsJob</span></span>
<span data-ttu-id="484ac-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="484ac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="484ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="484ac-120">-DefaultProfile</span></span>
<span data-ttu-id="484ac-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="484ac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="484ac-122">-Force</span><span class="sxs-lookup"><span data-stu-id="484ac-122">-Force</span></span>
<span data-ttu-id="484ac-123">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="484ac-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="484ac-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="484ac-124">-KeyId</span></span>
<span data-ttu-id="484ac-125">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="484ac-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="484ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="484ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="484ac-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="484ac-127">The name of the resource group</span></span>

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

### <span data-ttu-id="484ac-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="484ac-128">-ServerName</span></span>
<span data-ttu-id="484ac-129">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="484ac-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="484ac-130">-Type</span><span class="sxs-lookup"><span data-stu-id="484ac-130">-Type</span></span>
<span data-ttu-id="484ac-131">Typ funkcji Ochrona bazy danych usługi Azure Database TDE.</span><span class="sxs-lookup"><span data-stu-id="484ac-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="484ac-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="484ac-132">-Confirm</span></span>
<span data-ttu-id="484ac-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="484ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="484ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="484ac-134">-WhatIf</span></span>
<span data-ttu-id="484ac-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="484ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="484ac-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="484ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="484ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="484ac-137">CommonParameters</span></span>
<span data-ttu-id="484ac-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="484ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="484ac-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="484ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="484ac-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="484ac-140">INPUTS</span></span>

### <span data-ttu-id="484ac-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="484ac-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="484ac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="484ac-142">System.String</span></span>

## <span data-ttu-id="484ac-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="484ac-143">OUTPUTS</span></span>

### <span data-ttu-id="484ac-144">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="484ac-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="484ac-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="484ac-145">NOTES</span></span>

## <span data-ttu-id="484ac-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="484ac-146">RELATED LINKS</span></span>

[<span data-ttu-id="484ac-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="484ac-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
