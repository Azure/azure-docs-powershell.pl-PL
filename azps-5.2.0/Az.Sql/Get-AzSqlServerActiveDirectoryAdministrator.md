---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350110"
---
# <span data-ttu-id="ceff7-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceff7-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ceff7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ceff7-102">SYNOPSIS</span></span>
<span data-ttu-id="ceff7-103">Pobiera informacje o administratorze usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ceff7-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="ceff7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ceff7-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceff7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ceff7-105">DESCRIPTION</span></span>
<span data-ttu-id="ceff7-106">Polecenie cmdlet **Get-AzSqlServerActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ceff7-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ceff7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ceff7-107">EXAMPLES</span></span>

### <span data-ttu-id="ceff7-108">Przykład 1: Pobiera informacje o administratorze serwera</span><span class="sxs-lookup"><span data-stu-id="ceff7-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="ceff7-109">To polecenie pobiera informacje o administratorze usługi Azure AD dla serwera o nazwie Server01, który jest skojarzony z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ceff7-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ceff7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ceff7-110">PARAMETERS</span></span>

### <span data-ttu-id="ceff7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceff7-111">-DefaultProfile</span></span>
<span data-ttu-id="ceff7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ceff7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceff7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceff7-113">-ResourceGroupName</span></span>
<span data-ttu-id="ceff7-114">Określa nazwę grupy zasobów, do której jest przypisany serwer SQL.</span><span class="sxs-lookup"><span data-stu-id="ceff7-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ceff7-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ceff7-115">-ServerName</span></span>
<span data-ttu-id="ceff7-116">Określa nazwę serwera SQL, dla którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="ceff7-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ceff7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ceff7-117">-Confirm</span></span>
<span data-ttu-id="ceff7-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceff7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceff7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceff7-119">-WhatIf</span></span>
<span data-ttu-id="ceff7-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceff7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceff7-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ceff7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceff7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceff7-122">CommonParameters</span></span>
<span data-ttu-id="ceff7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceff7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceff7-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceff7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceff7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceff7-125">INPUTS</span></span>

### <span data-ttu-id="ceff7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ceff7-126">System.String</span></span>

## <span data-ttu-id="ceff7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ceff7-127">OUTPUTS</span></span>

### <span data-ttu-id="ceff7-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ceff7-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ceff7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ceff7-129">NOTES</span></span>

## <span data-ttu-id="ceff7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceff7-130">RELATED LINKS</span></span>

[<span data-ttu-id="ceff7-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceff7-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ceff7-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceff7-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ceff7-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ceff7-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ceff7-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ceff7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


