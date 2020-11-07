---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707790"
---
# <span data-ttu-id="17848-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17848-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="17848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17848-102">SYNOPSIS</span></span>
<span data-ttu-id="17848-103">Usuwa zasady wykrywania zagrożeń z serwera.</span><span class="sxs-lookup"><span data-stu-id="17848-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="17848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17848-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17848-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17848-105">DESCRIPTION</span></span>
<span data-ttu-id="17848-106">Polecenie cmdlet Remove-AzSqlServerThreatDetectionPolicy usuwa zasady wykrywania zagrożeń z programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17848-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="17848-107">Aby użyć tego polecenia cmdlet, określ parametry ResourceGroupName oraz nazwa_serwera w celu zidentyfikowania serwera, z którego to polecenie cmdlet usunie zasady.</span><span class="sxs-lookup"><span data-stu-id="17848-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="17848-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17848-108">EXAMPLES</span></span>

### <span data-ttu-id="17848-109">Przykład 1: usuwanie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="17848-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="17848-110">To polecenie usuwa zasady wykrywania zagrożeń z serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="17848-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="17848-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17848-111">PARAMETERS</span></span>

### <span data-ttu-id="17848-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17848-112">-DefaultProfile</span></span>
<span data-ttu-id="17848-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="17848-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17848-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17848-114">-PassThru</span></span>
<span data-ttu-id="17848-115">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="17848-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17848-116">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="17848-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17848-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17848-117">-ResourceGroupName</span></span>
<span data-ttu-id="17848-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="17848-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="17848-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="17848-119">-ServerName</span></span>
<span data-ttu-id="17848-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="17848-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17848-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17848-121">-Confirm</span></span>
<span data-ttu-id="17848-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17848-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17848-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17848-123">-WhatIf</span></span>
<span data-ttu-id="17848-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17848-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17848-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17848-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17848-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17848-126">CommonParameters</span></span>
<span data-ttu-id="17848-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17848-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17848-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17848-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17848-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17848-129">INPUTS</span></span>

### <span data-ttu-id="17848-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17848-130">System.String</span></span>

## <span data-ttu-id="17848-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17848-131">OUTPUTS</span></span>

### <span data-ttu-id="17848-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="17848-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="17848-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17848-133">NOTES</span></span>

## <span data-ttu-id="17848-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17848-134">RELATED LINKS</span></span>

[<span data-ttu-id="17848-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="17848-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

