---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ebd1fa17bfe35a4f0cb73d5ff3c3658e439abf78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545976"
---
# <span data-ttu-id="94674-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94674-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="94674-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94674-102">SYNOPSIS</span></span>
<span data-ttu-id="94674-103">Pobiera informacje o administratorze usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="94674-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94674-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94674-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94674-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94674-105">DESCRIPTION</span></span>
<span data-ttu-id="94674-106">Polecenie cmdlet **Get-AzureRmSqlServerActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="94674-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="94674-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94674-107">EXAMPLES</span></span>

### <span data-ttu-id="94674-108">Przykład 1: Pobiera informacje o administratorze serwera</span><span class="sxs-lookup"><span data-stu-id="94674-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="94674-109">To polecenie pobiera informacje o administratorze usługi Azure AD dla serwera o nazwie Server01, który jest skojarzony z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="94674-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="94674-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94674-110">PARAMETERS</span></span>

### <span data-ttu-id="94674-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94674-111">-ResourceGroupName</span></span>
<span data-ttu-id="94674-112">Określa nazwę grupy zasobów, do której jest przypisany serwer SQL.</span><span class="sxs-lookup"><span data-stu-id="94674-112">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="94674-113">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="94674-113">-ServerName</span></span>
<span data-ttu-id="94674-114">Określa nazwę serwera SQL, dla którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="94674-114">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="94674-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94674-115">-Confirm</span></span>
<span data-ttu-id="94674-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94674-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94674-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94674-117">-WhatIf</span></span>
<span data-ttu-id="94674-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94674-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94674-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94674-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94674-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94674-120">-DefaultProfile</span></span>
<span data-ttu-id="94674-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94674-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94674-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94674-122">CommonParameters</span></span>
<span data-ttu-id="94674-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94674-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94674-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94674-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94674-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94674-125">INPUTS</span></span>

## <span data-ttu-id="94674-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94674-126">OUTPUTS</span></span>

### <span data-ttu-id="94674-127">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="94674-127">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="94674-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94674-128">NOTES</span></span>

## <span data-ttu-id="94674-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94674-129">RELATED LINKS</span></span>

[<span data-ttu-id="94674-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94674-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="94674-131">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94674-131">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="94674-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="94674-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


