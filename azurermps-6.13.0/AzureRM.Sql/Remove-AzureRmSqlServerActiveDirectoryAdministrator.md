---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: c8b186c55161732a014e281162fa5d6131e72115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552004"
---
# <span data-ttu-id="7b5ec-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b5ec-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="7b5ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5ec-103">Usuwa administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b5ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b5ec-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b5ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5ec-106">Polecenie cmdlet **Remove-AzureRmSqlServerActiveDirectoryAdministrator** usuwa administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="7b5ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="7b5ec-108">Przykład 1: usuwanie administratora</span><span class="sxs-lookup"><span data-stu-id="7b5ec-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7b5ec-109">To polecenie usuwa administratora usługi Azure AD dla serwera o nazwie Server01 skojarzonego z grupą ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7b5ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="7b5ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5ec-111">-DefaultProfile</span></span>
<span data-ttu-id="7b5ec-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7b5ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b5ec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7b5ec-113">-Force</span></span>
<span data-ttu-id="7b5ec-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b5ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b5ec-116">Określa nazwę grupy zasobów, do której jest przypisany serwer SQL.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="7b5ec-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7b5ec-117">-ServerName</span></span>
<span data-ttu-id="7b5ec-118">Określa nazwę serwera SQL, dla którego to polecenie cmdlet usunie administratora.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="7b5ec-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b5ec-119">-Confirm</span></span>
<span data-ttu-id="7b5ec-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b5ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5ec-121">-WhatIf</span></span>
<span data-ttu-id="7b5ec-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b5ec-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b5ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5ec-124">CommonParameters</span></span>
<span data-ttu-id="7b5ec-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5ec-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b5ec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5ec-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b5ec-127">INPUTS</span></span>

### <span data-ttu-id="7b5ec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7b5ec-128">System.String</span></span>

## <span data-ttu-id="7b5ec-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b5ec-129">OUTPUTS</span></span>

### <span data-ttu-id="7b5ec-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="7b5ec-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="7b5ec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b5ec-131">NOTES</span></span>

## <span data-ttu-id="7b5ec-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b5ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b5ec-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b5ec-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7b5ec-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b5ec-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7b5ec-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7b5ec-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

