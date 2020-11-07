---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: b0ca96910d763cfcf40530ad99872e1e0d50ca31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707817"
---
# <span data-ttu-id="348fe-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="348fe-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="348fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="348fe-102">SYNOPSIS</span></span>
<span data-ttu-id="348fe-103">Usuwa zasady wykrywania zagrożeń z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="348fe-103">Removes the threat detection policy from a database.</span></span>

## <span data-ttu-id="348fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="348fe-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="348fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="348fe-105">DESCRIPTION</span></span>
<span data-ttu-id="348fe-106">Polecenie cmdlet **Remove-AzSqlDatabaseThreatDetectionPolicy** usuwa zasady wykrywania zagrożeń z bazy danych AzureAzure SQL.</span><span class="sxs-lookup"><span data-stu-id="348fe-106">The **Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="348fe-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania bazy danych, z której to polecenie cmdlet usunie zasady.</span><span class="sxs-lookup"><span data-stu-id="348fe-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="348fe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="348fe-108">EXAMPLES</span></span>

### <span data-ttu-id="348fe-109">Przykład 1: usuwanie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="348fe-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="348fe-110">To polecenie usuwa zasady wykrywania zagrożeń z bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="348fe-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="348fe-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="348fe-111">PARAMETERS</span></span>

### <span data-ttu-id="348fe-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="348fe-112">-DatabaseName</span></span>
<span data-ttu-id="348fe-113">Określa nazwę bazy danych, w której należy usunąć zasady wykrywania zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="348fe-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="348fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348fe-114">-DefaultProfile</span></span>
<span data-ttu-id="348fe-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="348fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="348fe-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="348fe-116">-PassThru</span></span>
<span data-ttu-id="348fe-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="348fe-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="348fe-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="348fe-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="348fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="348fe-120">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="348fe-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="348fe-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="348fe-121">-ServerName</span></span>
<span data-ttu-id="348fe-122">Określa nazwę serwera, na którym jest uruchamiana baza danych.</span><span class="sxs-lookup"><span data-stu-id="348fe-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="348fe-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="348fe-123">-Confirm</span></span>
<span data-ttu-id="348fe-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="348fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="348fe-125">-WhatIf</span></span>
<span data-ttu-id="348fe-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="348fe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="348fe-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="348fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348fe-128">CommonParameters</span></span>
<span data-ttu-id="348fe-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="348fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348fe-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="348fe-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348fe-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="348fe-131">INPUTS</span></span>

### <span data-ttu-id="348fe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="348fe-132">System.String</span></span>

## <span data-ttu-id="348fe-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="348fe-133">OUTPUTS</span></span>

### <span data-ttu-id="348fe-134">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="348fe-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="348fe-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="348fe-135">NOTES</span></span>

## <span data-ttu-id="348fe-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="348fe-136">RELATED LINKS</span></span>

[<span data-ttu-id="348fe-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="348fe-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

