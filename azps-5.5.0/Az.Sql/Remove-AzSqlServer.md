---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176818"
---
# <span data-ttu-id="3246f-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3246f-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="3246f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3246f-102">SYNOPSIS</span></span>
<span data-ttu-id="3246f-103">Usuwa serwer usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3246f-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="3246f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3246f-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3246f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3246f-105">DESCRIPTION</span></span>
<span data-ttu-id="3246f-106">Polecenie **cmdlet Remove-AzSqlServer** usuwa serwer usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3246f-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="3246f-107">Operacja usuwania jest asynchroniczna i może zająć trochę czasu, więc przed wykonaniem jakichkolwiek dodatkowych operacji, które zależą od całkowitego usunięcia serwera, sprawdź, czy operacja została ukończona.</span><span class="sxs-lookup"><span data-stu-id="3246f-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="3246f-108">Na przykład musisz utworzyć nowy serwer o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="3246f-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="3246f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3246f-109">EXAMPLES</span></span>

### <span data-ttu-id="3246f-110">Przykład 1. Usuwanie serwera</span><span class="sxs-lookup"><span data-stu-id="3246f-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3246f-111">To polecenie usuwa serwer usługi Azure SQL Database o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="3246f-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="3246f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3246f-112">PARAMETERS</span></span>

### <span data-ttu-id="3246f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3246f-113">-DefaultProfile</span></span>
<span data-ttu-id="3246f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3246f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3246f-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3246f-115">-Force</span></span>
<span data-ttu-id="3246f-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3246f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3246f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3246f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3246f-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="3246f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3246f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3246f-119">-ServerName</span></span>
<span data-ttu-id="3246f-120">Określa nazwę serwera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3246f-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3246f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3246f-121">-Confirm</span></span>
<span data-ttu-id="3246f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3246f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3246f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3246f-123">-WhatIf</span></span>
<span data-ttu-id="3246f-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3246f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3246f-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3246f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3246f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3246f-126">CommonParameters</span></span>
<span data-ttu-id="3246f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3246f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3246f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3246f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3246f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3246f-129">INPUTS</span></span>

### <span data-ttu-id="3246f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3246f-130">System.String</span></span>

## <span data-ttu-id="3246f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3246f-131">OUTPUTS</span></span>

### <span data-ttu-id="3246f-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3246f-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3246f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3246f-133">NOTES</span></span>

## <span data-ttu-id="3246f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3246f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3246f-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3246f-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="3246f-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3246f-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="3246f-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3246f-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="3246f-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3246f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


