---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063193"
---
# <span data-ttu-id="d3b05-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="d3b05-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="d3b05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3b05-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b05-103">Usuwa z bazy danych Zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="d3b05-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="d3b05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3b05-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d3b05-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b05-106">Polecenie cmdlet **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z bazy danych programu AzureAzure SQL.</span><span class="sxs-lookup"><span data-stu-id="d3b05-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="d3b05-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania bazy danych, z której to polecenie cmdlet usunie ustawienia.</span><span class="sxs-lookup"><span data-stu-id="d3b05-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="d3b05-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3b05-108">EXAMPLES</span></span>

### <span data-ttu-id="d3b05-109">Przykład 1: usuwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="d3b05-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d3b05-110">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="d3b05-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d3b05-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3b05-111">PARAMETERS</span></span>

### <span data-ttu-id="d3b05-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3b05-112">-DatabaseName</span></span>
<span data-ttu-id="d3b05-113">Określa nazwę bazy danych, w której należy usunąć zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="d3b05-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="d3b05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b05-114">-DefaultProfile</span></span>
<span data-ttu-id="d3b05-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d3b05-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3b05-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b05-116">-PassThru</span></span>
<span data-ttu-id="d3b05-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d3b05-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3b05-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d3b05-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3b05-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b05-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3b05-120">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="d3b05-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="d3b05-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d3b05-121">-ServerName</span></span>
<span data-ttu-id="d3b05-122">Określa nazwę serwera, na którym jest uruchamiana baza danych.</span><span class="sxs-lookup"><span data-stu-id="d3b05-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="d3b05-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3b05-123">-Confirm</span></span>
<span data-ttu-id="d3b05-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b05-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b05-125">-WhatIf</span></span>
<span data-ttu-id="d3b05-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3b05-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3b05-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3b05-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b05-128">CommonParameters</span></span>
<span data-ttu-id="d3b05-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3b05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b05-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3b05-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b05-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3b05-131">INPUTS</span></span>

### <span data-ttu-id="d3b05-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d3b05-132">System.String</span></span>

## <span data-ttu-id="d3b05-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3b05-133">OUTPUTS</span></span>

### <span data-ttu-id="d3b05-134">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="d3b05-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="d3b05-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3b05-135">NOTES</span></span>

## <span data-ttu-id="d3b05-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3b05-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3b05-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d3b05-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


