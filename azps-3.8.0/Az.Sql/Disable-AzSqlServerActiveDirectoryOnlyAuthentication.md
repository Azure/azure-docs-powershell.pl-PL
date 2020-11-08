---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050983"
---
# <span data-ttu-id="f6216-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f6216-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f6216-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6216-102">SYNOPSIS</span></span>
<span data-ttu-id="f6216-103">Wyłącza uwierzytelnianie tylko platformy Azure AD dla określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="f6216-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="f6216-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6216-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6216-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6216-105">DESCRIPTION</span></span>
<span data-ttu-id="f6216-106">Polecenie cmdlet **disable-AzSqlServerActiveDirectoryOnlyAuthentication** wyłącza tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f6216-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="f6216-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6216-107">EXAMPLES</span></span>

### <span data-ttu-id="f6216-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6216-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="f6216-109">To polecenie wyłącza tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla serwera AzureSQL o nazwie Server01, który jest skojarzony z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f6216-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f6216-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6216-110">PARAMETERS</span></span>

### <span data-ttu-id="f6216-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6216-111">-DefaultProfile</span></span>
<span data-ttu-id="f6216-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6216-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6216-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6216-113">-ResourceGroupName</span></span>
<span data-ttu-id="f6216-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6216-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6216-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f6216-115">-ServerName</span></span>
<span data-ttu-id="f6216-116">Nazwa programu Azure SQL Server, w którym znajduje się administrator usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6216-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6216-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6216-117">-Confirm</span></span>
<span data-ttu-id="f6216-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6216-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6216-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6216-119">-WhatIf</span></span>
<span data-ttu-id="f6216-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6216-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6216-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6216-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6216-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6216-122">CommonParameters</span></span>
<span data-ttu-id="f6216-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6216-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6216-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6216-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6216-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6216-125">INPUTS</span></span>

### <span data-ttu-id="f6216-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f6216-126">System.String</span></span>

## <span data-ttu-id="f6216-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6216-127">OUTPUTS</span></span>

### <span data-ttu-id="f6216-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="f6216-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="f6216-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6216-129">NOTES</span></span>

## <span data-ttu-id="f6216-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6216-130">RELATED LINKS</span></span>

[<span data-ttu-id="f6216-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6216-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f6216-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6216-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f6216-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6216-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f6216-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f6216-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
