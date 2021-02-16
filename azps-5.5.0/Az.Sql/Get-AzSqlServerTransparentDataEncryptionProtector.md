---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201475"
---
# <span data-ttu-id="cf8fa-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cf8fa-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="cf8fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8fa-103">Pobiera szyfrowanie przezroczystych danych (TDE, Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="cf8fa-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="cf8fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf8fa-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8fa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf8fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8fa-106">Polecenie Get-AzSqlServerTransparentDataEncryptionProtector cmdlet pobiera informacje na temat TDE.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="cf8fa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf8fa-107">EXAMPLES</span></span>

### <span data-ttu-id="cf8fa-108">Przykład 1. Uzyskiwanie transparentnego szyfrowania danych (TDE, Transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="cf8fa-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="cf8fa-109">To polecenie pobiera nazwę TDE serwera o nazwie ContosoServer w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="cf8fa-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="cf8fa-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="cf8fa-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="cf8fa-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="cf8fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf8fa-112">PARAMETERS</span></span>

### <span data-ttu-id="cf8fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8fa-113">-DefaultProfile</span></span>
<span data-ttu-id="cf8fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cf8fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf8fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf8fa-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cf8fa-116">The name of the resource group</span></span>

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

### <span data-ttu-id="cf8fa-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf8fa-117">-ServerName</span></span>
<span data-ttu-id="cf8fa-118">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cf8fa-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf8fa-119">-Confirm</span></span>
<span data-ttu-id="cf8fa-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf8fa-121">-WhatIf</span></span>
<span data-ttu-id="cf8fa-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf8fa-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8fa-124">CommonParameters</span></span>
<span data-ttu-id="cf8fa-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8fa-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf8fa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8fa-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf8fa-127">INPUTS</span></span>

### <span data-ttu-id="cf8fa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cf8fa-128">System.String</span></span>

## <span data-ttu-id="cf8fa-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf8fa-129">OUTPUTS</span></span>

### <span data-ttu-id="cf8fa-130">Microsoft.Azure.Commands.sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="cf8fa-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="cf8fa-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf8fa-131">NOTES</span></span>

## <span data-ttu-id="cf8fa-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf8fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf8fa-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="cf8fa-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
