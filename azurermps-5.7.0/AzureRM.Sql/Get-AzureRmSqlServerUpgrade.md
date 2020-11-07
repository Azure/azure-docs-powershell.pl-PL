---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c1be584b1110f720d1d5d50b32d7efa5d8586db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718421"
---
# <span data-ttu-id="30a51-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="30a51-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="30a51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30a51-102">SYNOPSIS</span></span>
<span data-ttu-id="30a51-103">Pobiera stan uaktualnienia serwera bazy danych SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30a51-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30a51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30a51-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30a51-105">DESCRIPTION</span></span>
<span data-ttu-id="30a51-106">Polecenie cmdlet **Get-AzureRmSqlServerUpgrade** Pobiera stan uaktualnienia serwera bazy danych SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30a51-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="30a51-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30a51-107">EXAMPLES</span></span>

### <span data-ttu-id="30a51-108">Przykład 1: uzyskiwanie statusu uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="30a51-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="30a51-109">To polecenie uzyskuje stan uaktualnienia z serwera o nazwie Server01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="30a51-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="30a51-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30a51-110">PARAMETERS</span></span>

### <span data-ttu-id="30a51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a51-111">-DefaultProfile</span></span>
<span data-ttu-id="30a51-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="30a51-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30a51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a51-113">-ResourceGroupName</span></span>
<span data-ttu-id="30a51-114">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="30a51-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="30a51-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="30a51-115">-ServerName</span></span>
<span data-ttu-id="30a51-116">Określa nazwę serwera, dla którego ten aplet polecenia Pobiera stan uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="30a51-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="30a51-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30a51-117">-Confirm</span></span>
<span data-ttu-id="30a51-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a51-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a51-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a51-119">-WhatIf</span></span>
<span data-ttu-id="30a51-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a51-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a51-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30a51-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a51-122">CommonParameters</span></span>
<span data-ttu-id="30a51-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a51-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30a51-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a51-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a51-125">INPUTS</span></span>

### <span data-ttu-id="30a51-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30a51-126">None</span></span>
<span data-ttu-id="30a51-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="30a51-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30a51-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30a51-128">OUTPUTS</span></span>

### <span data-ttu-id="30a51-129">Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="30a51-129">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="30a51-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30a51-130">NOTES</span></span>

## <span data-ttu-id="30a51-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a51-131">RELATED LINKS</span></span>

[<span data-ttu-id="30a51-132">Start — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="30a51-132">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="30a51-133">Zatrzymaj — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="30a51-133">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="30a51-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="30a51-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


