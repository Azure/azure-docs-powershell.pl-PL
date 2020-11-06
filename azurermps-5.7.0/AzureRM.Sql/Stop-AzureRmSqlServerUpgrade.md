---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524801"
---
# <span data-ttu-id="6ff80-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ff80-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="6ff80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ff80-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff80-103">Zatrzymuje uaktualnienie serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6ff80-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ff80-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ff80-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff80-106">Polecenie cmdlet **stop-AzureRmSqlServerUpgrade** zatrzymuje uaktualnianie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff80-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="6ff80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ff80-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff80-108">Przykład 1: zatrzymywanie uaktualnienia serwera</span><span class="sxs-lookup"><span data-stu-id="6ff80-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="6ff80-109">To polecenie zatrzymuje żądanie uaktualnienia serwera o nazwie Server02 przypisanego do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6ff80-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6ff80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ff80-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff80-111">-DefaultProfile</span></span>
<span data-ttu-id="6ff80-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6ff80-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6ff80-113">-Force</span></span>
<span data-ttu-id="6ff80-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6ff80-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff80-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ff80-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="6ff80-116">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6ff80-117">-ServerName</span></span>
<span data-ttu-id="6ff80-118">Określa nazwę serwera, dla którego to polecenie cmdlet zatrzymuje uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="6ff80-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ff80-119">-Confirm</span></span>
<span data-ttu-id="6ff80-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff80-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff80-121">-WhatIf</span></span>
<span data-ttu-id="6ff80-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff80-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff80-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ff80-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff80-124">CommonParameters</span></span>
<span data-ttu-id="6ff80-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff80-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff80-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ff80-127">INPUTS</span></span>

### <span data-ttu-id="6ff80-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="6ff80-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="6ff80-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ff80-129">OUTPUTS</span></span>

## <span data-ttu-id="6ff80-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ff80-130">NOTES</span></span>

## <span data-ttu-id="6ff80-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ff80-131">RELATED LINKS</span></span>

[<span data-ttu-id="6ff80-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ff80-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="6ff80-133">Start — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ff80-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="6ff80-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6ff80-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


