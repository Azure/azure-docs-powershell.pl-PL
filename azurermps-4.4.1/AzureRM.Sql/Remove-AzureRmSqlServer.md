---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554185"
---
# <span data-ttu-id="26cb9-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26cb9-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="26cb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="26cb9-103">Usuwa serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26cb9-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26cb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26cb9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26cb9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="26cb9-106">Polecenie cmdlet **Remove-AzureRmSqlServer** usuwa serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26cb9-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="26cb9-107">Operacja usuwania jest asynchroniczna i może trochę potrwać, dlatego przed wykonaniem wszystkich dodatkowych operacji zależnych od serwera całkowicie usuniętego należy sprawdzić, czy operacja została zakończona.</span><span class="sxs-lookup"><span data-stu-id="26cb9-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="26cb9-108">Na przykład trzeba utworzyć nowy serwer używający tej samej nazwy.</span><span class="sxs-lookup"><span data-stu-id="26cb9-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="26cb9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="26cb9-110">Przykład 1: Usuwanie serwera</span><span class="sxs-lookup"><span data-stu-id="26cb9-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="26cb9-111">To polecenie usuwa serwer bazy danych SQL Azure o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="26cb9-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="26cb9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26cb9-112">PARAMETERS</span></span>

### <span data-ttu-id="26cb9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26cb9-113">-Force</span></span>
<span data-ttu-id="26cb9-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="26cb9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26cb9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26cb9-115">-ResourceGroupName</span></span>
<span data-ttu-id="26cb9-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="26cb9-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="26cb9-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="26cb9-117">-ServerName</span></span>
<span data-ttu-id="26cb9-118">Określa nazwę serwera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="26cb9-118">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="26cb9-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26cb9-119">-Confirm</span></span>
<span data-ttu-id="26cb9-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26cb9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26cb9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26cb9-121">-WhatIf</span></span>
<span data-ttu-id="26cb9-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26cb9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26cb9-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26cb9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26cb9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cb9-124">-DefaultProfile</span></span>
<span data-ttu-id="26cb9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26cb9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26cb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cb9-126">CommonParameters</span></span>
<span data-ttu-id="26cb9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26cb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cb9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26cb9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26cb9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26cb9-129">INPUTS</span></span>

### <span data-ttu-id="26cb9-130">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="26cb9-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="26cb9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26cb9-131">OUTPUTS</span></span>

### <span data-ttu-id="26cb9-132">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="26cb9-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="26cb9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26cb9-133">NOTES</span></span>

## <span data-ttu-id="26cb9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26cb9-134">RELATED LINKS</span></span>

[<span data-ttu-id="26cb9-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26cb9-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="26cb9-136">Nowe — AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26cb9-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="26cb9-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26cb9-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="26cb9-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="26cb9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


