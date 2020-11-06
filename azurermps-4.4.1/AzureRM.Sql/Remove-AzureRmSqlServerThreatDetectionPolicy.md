---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528193"
---
# <span data-ttu-id="473f9-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="473f9-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="473f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="473f9-102">SYNOPSIS</span></span>
<span data-ttu-id="473f9-103">Usuwa zasady wykrywania zagrożeń z serwera.</span><span class="sxs-lookup"><span data-stu-id="473f9-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="473f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="473f9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="473f9-105">DESCRIPTION</span></span>
<span data-ttu-id="473f9-106">Polecenie cmdlet Remove-AzureRmSqlServerThreatDetectionPolicy usuwa zasady wykrywania zagrożeń z programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="473f9-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="473f9-107">Aby użyć tego polecenia cmdlet, określ parametry ResourceGroupName oraz nazwa_serwera w celu zidentyfikowania serwera, z którego to polecenie cmdlet usunie zasady.</span><span class="sxs-lookup"><span data-stu-id="473f9-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="473f9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="473f9-108">EXAMPLES</span></span>

### <span data-ttu-id="473f9-109">--------------------------Przykład 1: usuwanie zasad wykrywania zagrożeń dla bazy danych--------------------------</span><span class="sxs-lookup"><span data-stu-id="473f9-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="473f9-110">To polecenie usuwa zasady wykrywania zagrożeń z serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="473f9-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="473f9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="473f9-111">PARAMETERS</span></span>

### <span data-ttu-id="473f9-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="473f9-112">-PassThru</span></span>
<span data-ttu-id="473f9-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="473f9-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="473f9-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="473f9-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="473f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="473f9-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="473f9-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="473f9-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="473f9-117">-ServerName</span></span>
<span data-ttu-id="473f9-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="473f9-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="473f9-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="473f9-119">-Confirm</span></span>
<span data-ttu-id="473f9-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="473f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473f9-121">-WhatIf</span></span>
<span data-ttu-id="473f9-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="473f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="473f9-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="473f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="473f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473f9-124">-DefaultProfile</span></span>
<span data-ttu-id="473f9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="473f9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="473f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473f9-126">CommonParameters</span></span>
<span data-ttu-id="473f9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473f9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473f9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="473f9-129">INPUTS</span></span>

###  
<span data-ttu-id="473f9-130">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="473f9-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="473f9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="473f9-131">OUTPUTS</span></span>

### <span data-ttu-id="473f9-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="473f9-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="473f9-133">To polecenie cmdlet zwraca obiekt ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="473f9-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="473f9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="473f9-134">NOTES</span></span>

## <span data-ttu-id="473f9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="473f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="473f9-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="473f9-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

