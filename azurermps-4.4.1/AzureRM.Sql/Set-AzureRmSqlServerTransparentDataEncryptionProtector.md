---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719497"
---
# <span data-ttu-id="0ad9c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0ad9c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="0ad9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad9c-103">Ustawia funkcję ochrony przezroczystego szyfrowania danych (TDE) dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ad9c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ad9c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad9c-106">Polecenie cmdlet Set-AzureRmSqlServerTransparentDataEncryptionProtector ustawia ochronę TDE dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="0ad9c-107">Zmiana typu funkcji ochrony TDE spowoduje obrócenie funkcji ochrony.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="0ad9c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ad9c-108">EXAMPLES</span></span>

### <span data-ttu-id="0ad9c-109">--------------------------Przykład 1: Ustawianie typu funkcji Ochrona danych przezroczystego szyfrowania (TDE) na wartość servicemanage--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ad9c-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="0ad9c-110">To polecenie aktualizuje typ funkcji Ochrona TDE serwera na wartość zarządzana przez usługę.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="0ad9c-111">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="0ad9c-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="0ad9c-112">ContosoResourceGroup ContosoServer servicemanage</span><span class="sxs-lookup"><span data-stu-id="0ad9c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="0ad9c-113">--------------------------Przykład 2: Ustaw typ ochrony szyfrowania danych przezroczystych na magazyn kluczy platformy Azure--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ad9c-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="0ad9c-114">To polecenie aktualizuje serwer w celu użycia klucza magazynu kluczy serwera o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="0ad9c-115">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="0ad9c-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="0ad9c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="0ad9c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="0ad9c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ad9c-117">PARAMETERS</span></span>

### <span data-ttu-id="0ad9c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0ad9c-118">-Force</span></span>
<span data-ttu-id="0ad9c-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="0ad9c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0ad9c-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="0ad9c-120">-KeyId</span></span>
<span data-ttu-id="0ad9c-121">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="0ad9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ad9c-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ad9c-123">The name of the resource group</span></span>

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

### <span data-ttu-id="0ad9c-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0ad9c-124">-ServerName</span></span>
<span data-ttu-id="0ad9c-125">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0ad9c-126">-Type</span><span class="sxs-lookup"><span data-stu-id="0ad9c-126">-Type</span></span>
<span data-ttu-id="0ad9c-127">Typ funkcji Ochrona bazy danych usługi Azure Database TDE.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="0ad9c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ad9c-128">-Confirm</span></span>
<span data-ttu-id="0ad9c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad9c-130">-WhatIf</span></span>
<span data-ttu-id="0ad9c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad9c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad9c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad9c-133">-DefaultProfile</span></span>
<span data-ttu-id="0ad9c-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad9c-135">CommonParameters</span></span>
<span data-ttu-id="0ad9c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad9c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad9c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad9c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ad9c-138">INPUTS</span></span>

### <span data-ttu-id="0ad9c-139">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="0ad9c-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="0ad9c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad9c-140">System.String</span></span>

## <span data-ttu-id="0ad9c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ad9c-141">OUTPUTS</span></span>

### <span data-ttu-id="0ad9c-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="0ad9c-142">System.Object</span></span>

## <span data-ttu-id="0ad9c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ad9c-143">NOTES</span></span>

## <span data-ttu-id="0ad9c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ad9c-144">RELATED LINKS</span></span>

[<span data-ttu-id="0ad9c-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0ad9c-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
