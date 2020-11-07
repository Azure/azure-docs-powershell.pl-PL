---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: c1571dd5d03f82da13feec115fb9da123c6e3f69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707897"
---
# <span data-ttu-id="68f95-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="68f95-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="68f95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68f95-102">SYNOPSIS</span></span>
<span data-ttu-id="68f95-103">Pobiera funkcję ochrony przezroczystego szyfrowania danych (TDE)</span><span class="sxs-lookup"><span data-stu-id="68f95-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="68f95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68f95-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68f95-105">DESCRIPTION</span></span>
<span data-ttu-id="68f95-106">Polecenie cmdlet Get-AzSqlServerTransparentDataEncryptionProtector pobiera informacje o funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="68f95-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="68f95-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68f95-107">EXAMPLES</span></span>

### <span data-ttu-id="68f95-108">Przykład 1: uzyskiwanie funkcji ochrony przezroczystego szyfrowania danych (TDE)</span><span class="sxs-lookup"><span data-stu-id="68f95-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="68f95-109">To polecenie pobiera ochronę TDE dla serwera o nazwie ContosoServer w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68f95-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="68f95-110">ResourceGroupName nazwa_serwera typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="68f95-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="68f95-111">ContosoResourceGroup ContosoServer servicemanage</span><span class="sxs-lookup"><span data-stu-id="68f95-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="68f95-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68f95-112">PARAMETERS</span></span>

### <span data-ttu-id="68f95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f95-113">-DefaultProfile</span></span>
<span data-ttu-id="68f95-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68f95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68f95-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f95-115">-ResourceGroupName</span></span>
<span data-ttu-id="68f95-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="68f95-116">The name of the resource group</span></span>

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

### <span data-ttu-id="68f95-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="68f95-117">-ServerName</span></span>
<span data-ttu-id="68f95-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68f95-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="68f95-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68f95-119">-Confirm</span></span>
<span data-ttu-id="68f95-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f95-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f95-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f95-121">-WhatIf</span></span>
<span data-ttu-id="68f95-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f95-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f95-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68f95-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f95-124">CommonParameters</span></span>
<span data-ttu-id="68f95-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f95-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68f95-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f95-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68f95-127">INPUTS</span></span>

### <span data-ttu-id="68f95-128">System. String</span><span class="sxs-lookup"><span data-stu-id="68f95-128">System.String</span></span>

## <span data-ttu-id="68f95-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68f95-129">OUTPUTS</span></span>

### <span data-ttu-id="68f95-130">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="68f95-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="68f95-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68f95-131">NOTES</span></span>

## <span data-ttu-id="68f95-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68f95-132">RELATED LINKS</span></span>

[<span data-ttu-id="68f95-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="68f95-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)