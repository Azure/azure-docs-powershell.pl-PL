---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553750"
---
# <span data-ttu-id="0c36e-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c36e-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="0c36e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c36e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c36e-103">Dodaje klucz magazynu kluczy do programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c36e-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c36e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c36e-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c36e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c36e-105">DESCRIPTION</span></span>
<span data-ttu-id="0c36e-106">Polecenie cmdlet Add-AzureRmSqlServerKeyVaultKey dodaje klucz magazynu kluczy do dostarczonego programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c36e-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="0c36e-107">Serwer musi mieć uprawnienia Get, wrapKey, unwrapKey ' do magazynu.</span><span class="sxs-lookup"><span data-stu-id="0c36e-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="0c36e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c36e-108">EXAMPLES</span></span>

### <span data-ttu-id="0c36e-109">--------------------------Przykład 1: Dodawanie klucza magazynu kluczy--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c36e-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="0c36e-110">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do programu SQL Server o nazwie "ContosoServer" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="0c36e-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="0c36e-111">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="0c36e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="0c36e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c36e-112">PARAMETERS</span></span>

### <span data-ttu-id="0c36e-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="0c36e-113">-KeyId</span></span>
<span data-ttu-id="0c36e-114">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="0c36e-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="0c36e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c36e-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c36e-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c36e-116">The name of the resource group</span></span>

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

### <span data-ttu-id="0c36e-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0c36e-117">-ServerName</span></span>
<span data-ttu-id="0c36e-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c36e-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0c36e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c36e-119">-Confirm</span></span>
<span data-ttu-id="0c36e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c36e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c36e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c36e-121">-WhatIf</span></span>
<span data-ttu-id="0c36e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c36e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c36e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c36e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c36e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c36e-124">-DefaultProfile</span></span>
<span data-ttu-id="0c36e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c36e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c36e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c36e-126">CommonParameters</span></span>
<span data-ttu-id="0c36e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c36e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c36e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c36e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c36e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c36e-129">INPUTS</span></span>

### <span data-ttu-id="0c36e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0c36e-130">System.String</span></span>

## <span data-ttu-id="0c36e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c36e-131">OUTPUTS</span></span>

### <span data-ttu-id="0c36e-132">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="0c36e-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="0c36e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c36e-133">NOTES</span></span>

## <span data-ttu-id="0c36e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c36e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c36e-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0c36e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
