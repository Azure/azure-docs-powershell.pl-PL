---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716655"
---
# <span data-ttu-id="b59de-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b59de-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="b59de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b59de-102">SYNOPSIS</span></span>
<span data-ttu-id="b59de-103">Usuwa klucz magazynu kluczy z programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b59de-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b59de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b59de-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b59de-105">DESCRIPTION</span></span>
<span data-ttu-id="b59de-106">Polecenie cmdlet Remove-AzureRmSqlServerKeyVaultKey usuwa klucz magazynu kluczy z określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="b59de-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="b59de-107">Zauważ, że uprawnienia programu SQL Server do magazynu kluczy nie są zmieniane.</span><span class="sxs-lookup"><span data-stu-id="b59de-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="b59de-108">Aby zmienić uprawnienia, użyj ustawienia Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="b59de-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="b59de-109">Pamiętaj, że to polecenie cmdlet nie wprowadza żadnych zmian w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b59de-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="b59de-110">Aby usunąć klucz z magazynu kluczy, użyj przycisku Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="b59de-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="b59de-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b59de-111">EXAMPLES</span></span>

### <span data-ttu-id="b59de-112">--------------------------Przykład 1: Usuwanie klucza magazynu kluczy--------------------------</span><span class="sxs-lookup"><span data-stu-id="b59de-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b59de-113">To polecenie powoduje usunięcie klucza magazynu kluczy o identyfikatorze z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="b59de-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="b59de-114">ResourceGroupName: ContosoResourceGroup nazwa_serwera: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 odcisk palca: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="b59de-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="b59de-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b59de-115">PARAMETERS</span></span>

### <span data-ttu-id="b59de-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b59de-116">-KeyId</span></span>
<span data-ttu-id="b59de-117">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="b59de-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="b59de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59de-118">-ResourceGroupName</span></span>
<span data-ttu-id="b59de-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b59de-119">The name of the resource group</span></span>

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

### <span data-ttu-id="b59de-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b59de-120">-ServerName</span></span>
<span data-ttu-id="b59de-121">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b59de-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b59de-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b59de-122">-Confirm</span></span>
<span data-ttu-id="b59de-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b59de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b59de-124">-WhatIf</span></span>
<span data-ttu-id="b59de-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b59de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b59de-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b59de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59de-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59de-127">-DefaultProfile</span></span>
<span data-ttu-id="b59de-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b59de-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b59de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59de-129">CommonParameters</span></span>
<span data-ttu-id="b59de-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59de-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59de-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b59de-132">INPUTS</span></span>

### <span data-ttu-id="b59de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b59de-133">System.String</span></span>

## <span data-ttu-id="b59de-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b59de-134">OUTPUTS</span></span>

### <span data-ttu-id="b59de-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="b59de-135">System.Object</span></span>

## <span data-ttu-id="b59de-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b59de-136">NOTES</span></span>

## <span data-ttu-id="b59de-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b59de-137">RELATED LINKS</span></span>

[<span data-ttu-id="b59de-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b59de-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
