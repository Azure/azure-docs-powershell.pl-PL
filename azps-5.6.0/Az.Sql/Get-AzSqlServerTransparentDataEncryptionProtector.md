---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: cd211537949fe3743298ad4cba93ca6c63b7c39b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003073"
---
# <span data-ttu-id="cb7ff-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb7ff-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="cb7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7ff-103">Pobiera szyfrowanie przezroczystych danych (TDE, Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="cb7ff-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="cb7ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb7ff-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb7ff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="cb7ff-106">Polecenie Get-AzSqlServerTransparentDataEncryptionProtector cmdlet pobiera informacje na temat TDE.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="cb7ff-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb7ff-107">EXAMPLES</span></span>

### <span data-ttu-id="cb7ff-108">Przykład 1. Uzyskiwanie transparentnego szyfrowania danych (TDE, Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="cb7ff-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="cb7ff-109">To polecenie pobiera nazwę TDE serwera o nazwie ContosoServer w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="cb7ff-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="cb7ff-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="cb7ff-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="cb7ff-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="cb7ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb7ff-112">PARAMETERS</span></span>

### <span data-ttu-id="cb7ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7ff-113">-DefaultProfile</span></span>
<span data-ttu-id="cb7ff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cb7ff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb7ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb7ff-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cb7ff-116">The name of the resource group</span></span>

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

### <span data-ttu-id="cb7ff-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb7ff-117">-ServerName</span></span>
<span data-ttu-id="cb7ff-118">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cb7ff-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb7ff-119">-Confirm</span></span>
<span data-ttu-id="cb7ff-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb7ff-121">-WhatIf</span></span>
<span data-ttu-id="cb7ff-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb7ff-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ff-124">CommonParameters</span></span>
<span data-ttu-id="cb7ff-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ff-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb7ff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ff-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb7ff-127">INPUTS</span></span>

### <span data-ttu-id="cb7ff-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cb7ff-128">System.String</span></span>

## <span data-ttu-id="cb7ff-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb7ff-129">OUTPUTS</span></span>

### <span data-ttu-id="cb7ff-130">Microsoft.Azure.Commands.sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="cb7ff-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="cb7ff-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb7ff-131">NOTES</span></span>

## <span data-ttu-id="cb7ff-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb7ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="cb7ff-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="cb7ff-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
