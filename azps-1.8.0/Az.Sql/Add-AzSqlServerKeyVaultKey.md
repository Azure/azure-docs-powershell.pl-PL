---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708046"
---
# <span data-ttu-id="c165d-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c165d-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="c165d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c165d-102">SYNOPSIS</span></span>
<span data-ttu-id="c165d-103">Dodaje klucz magazynu kluczy do programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c165d-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="c165d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c165d-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c165d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c165d-105">DESCRIPTION</span></span>
<span data-ttu-id="c165d-106">Polecenie cmdlet Add-AzSqlServerKeyVaultKey dodaje klucz magazynu kluczy do dostarczonego programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c165d-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="c165d-107">Serwer musi mieć uprawnienia Get, wrapKey, unwrapKey ' do magazynu.</span><span class="sxs-lookup"><span data-stu-id="c165d-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="c165d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c165d-108">EXAMPLES</span></span>

### <span data-ttu-id="c165d-109">Przykład 1: Dodawanie klucza magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="c165d-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c165d-110">To polecenie powoduje dodanie klucza magazynu kluczy o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " do programu SQL Server o nazwie "ContosoServer" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c165d-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="c165d-111">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="c165d-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="c165d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c165d-112">PARAMETERS</span></span>

### <span data-ttu-id="c165d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c165d-113">-AsJob</span></span>
<span data-ttu-id="c165d-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c165d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c165d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c165d-115">-DefaultProfile</span></span>
<span data-ttu-id="c165d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c165d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c165d-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c165d-117">-KeyId</span></span>
<span data-ttu-id="c165d-118">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="c165d-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c165d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c165d-119">-ResourceGroupName</span></span>
<span data-ttu-id="c165d-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c165d-120">The name of the resource group</span></span>

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

### <span data-ttu-id="c165d-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c165d-121">-ServerName</span></span>
<span data-ttu-id="c165d-122">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c165d-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c165d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c165d-123">-Confirm</span></span>
<span data-ttu-id="c165d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c165d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c165d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c165d-125">-WhatIf</span></span>
<span data-ttu-id="c165d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c165d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c165d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c165d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c165d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c165d-128">CommonParameters</span></span>
<span data-ttu-id="c165d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c165d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c165d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c165d-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c165d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c165d-131">INPUTS</span></span>

### <span data-ttu-id="c165d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c165d-132">System.String</span></span>

## <span data-ttu-id="c165d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c165d-133">OUTPUTS</span></span>

### <span data-ttu-id="c165d-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="c165d-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="c165d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c165d-135">NOTES</span></span>

## <span data-ttu-id="c165d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c165d-136">RELATED LINKS</span></span>

[<span data-ttu-id="c165d-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c165d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
