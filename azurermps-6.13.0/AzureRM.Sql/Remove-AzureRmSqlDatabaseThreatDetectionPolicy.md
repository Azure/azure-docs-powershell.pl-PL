---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 9b51a9e835962ea1715a458ace1ab02202068e30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548476"
---
# <span data-ttu-id="402ee-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="402ee-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="402ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="402ee-102">SYNOPSIS</span></span>
<span data-ttu-id="402ee-103">Usuwa zasady wykrywania zagrożeń z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="402ee-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="402ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="402ee-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="402ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="402ee-105">DESCRIPTION</span></span>
<span data-ttu-id="402ee-106">Polecenie cmdlet **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** usuwa zasady wykrywania zagrożeń z bazy danych AzureAzure SQL.</span><span class="sxs-lookup"><span data-stu-id="402ee-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="402ee-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania bazy danych, z której to polecenie cmdlet usunie zasady.</span><span class="sxs-lookup"><span data-stu-id="402ee-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="402ee-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="402ee-108">EXAMPLES</span></span>

### <span data-ttu-id="402ee-109">Przykład 1: usuwanie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="402ee-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="402ee-110">To polecenie usuwa zasady wykrywania zagrożeń z bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="402ee-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="402ee-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="402ee-111">PARAMETERS</span></span>

### <span data-ttu-id="402ee-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="402ee-112">-DatabaseName</span></span>
<span data-ttu-id="402ee-113">Określa nazwę bazy danych, w której należy usunąć zasady wykrywania zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="402ee-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="402ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402ee-114">-DefaultProfile</span></span>
<span data-ttu-id="402ee-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="402ee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="402ee-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="402ee-116">-PassThru</span></span>
<span data-ttu-id="402ee-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="402ee-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="402ee-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="402ee-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="402ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="402ee-120">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="402ee-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="402ee-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="402ee-121">-ServerName</span></span>
<span data-ttu-id="402ee-122">Określa nazwę serwera, na którym jest uruchamiana baza danych.</span><span class="sxs-lookup"><span data-stu-id="402ee-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="402ee-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="402ee-123">-Confirm</span></span>
<span data-ttu-id="402ee-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402ee-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402ee-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402ee-125">-WhatIf</span></span>
<span data-ttu-id="402ee-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402ee-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="402ee-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="402ee-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402ee-128">CommonParameters</span></span>
<span data-ttu-id="402ee-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402ee-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="402ee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402ee-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="402ee-131">INPUTS</span></span>

### <span data-ttu-id="402ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="402ee-132">System.String</span></span>

## <span data-ttu-id="402ee-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="402ee-133">OUTPUTS</span></span>

### <span data-ttu-id="402ee-134">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="402ee-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="402ee-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="402ee-135">NOTES</span></span>

## <span data-ttu-id="402ee-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="402ee-136">RELATED LINKS</span></span>

[<span data-ttu-id="402ee-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="402ee-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


