---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220271"
---
# <span data-ttu-id="e4b63-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e4b63-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="e4b63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4b63-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b63-103">Usuwa serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b63-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="e4b63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4b63-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4b63-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b63-106">Polecenie cmdlet **Remove-AzSqlServer** usuwa serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b63-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="e4b63-107">Operacja usuwania jest asynchroniczna i może trochę potrwać, dlatego przed wykonaniem wszystkich dodatkowych operacji zależnych od serwera całkowicie usuniętego należy sprawdzić, czy operacja została zakończona.</span><span class="sxs-lookup"><span data-stu-id="e4b63-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="e4b63-108">Na przykład trzeba utworzyć nowy serwer używający tej samej nazwy.</span><span class="sxs-lookup"><span data-stu-id="e4b63-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="e4b63-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4b63-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b63-110">Przykład 1: Usuwanie serwera</span><span class="sxs-lookup"><span data-stu-id="e4b63-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e4b63-111">To polecenie usuwa serwer bazy danych SQL Azure o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="e4b63-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="e4b63-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4b63-112">PARAMETERS</span></span>

### <span data-ttu-id="e4b63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b63-113">-DefaultProfile</span></span>
<span data-ttu-id="e4b63-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4b63-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4b63-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4b63-115">-Force</span></span>
<span data-ttu-id="e4b63-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4b63-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4b63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b63-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4b63-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="e4b63-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e4b63-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e4b63-119">-ServerName</span></span>
<span data-ttu-id="e4b63-120">Określa nazwę serwera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e4b63-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="e4b63-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4b63-121">-Confirm</span></span>
<span data-ttu-id="e4b63-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b63-123">-WhatIf</span></span>
<span data-ttu-id="e4b63-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b63-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4b63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b63-126">CommonParameters</span></span>
<span data-ttu-id="e4b63-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b63-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4b63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b63-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4b63-129">INPUTS</span></span>

### <span data-ttu-id="e4b63-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b63-130">System.String</span></span>

## <span data-ttu-id="e4b63-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4b63-131">OUTPUTS</span></span>

### <span data-ttu-id="e4b63-132">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e4b63-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e4b63-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4b63-133">NOTES</span></span>

## <span data-ttu-id="e4b63-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4b63-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4b63-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e4b63-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="e4b63-136">Nowe — AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e4b63-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e4b63-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e4b63-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="e4b63-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e4b63-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


