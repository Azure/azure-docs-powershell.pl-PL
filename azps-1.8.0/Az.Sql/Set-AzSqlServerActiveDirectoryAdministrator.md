---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 44339cb39396b18660d17bdbad0e597ded30ad18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707726"
---
# <span data-ttu-id="21db2-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21db2-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="21db2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21db2-102">SYNOPSIS</span></span>
<span data-ttu-id="21db2-103">Inicjuje obsługę administracyjną administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21db2-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="21db2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21db2-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21db2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21db2-105">DESCRIPTION</span></span>
<span data-ttu-id="21db2-106">Polecenie cmdlet **Set-AzSqlServerActiveDirectoryAdministrator** inicjuje administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="21db2-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="21db2-107">Możesz dostarczać tylko jednego administratora naraz.</span><span class="sxs-lookup"><span data-stu-id="21db2-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="21db2-108">W przypadku administratora programu SQL Server można zainicjować obsługę następujących członków usługi Azure AD:</span><span class="sxs-lookup"><span data-stu-id="21db2-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="21db2-109">Natywni członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="21db2-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="21db2-110">Federacyjny członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="21db2-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="21db2-111">Zaimportowani członkowie z innych reklam usługi Azure, którzy są członkami macierzystymi lub federacyjnymi</span><span class="sxs-lookup"><span data-stu-id="21db2-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="21db2-112">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń konta Microsoft, takie jak te w domenach Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="21db2-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="21db2-113">Inne konta Gości, takie jak te w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="21db2-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="21db2-114">Zalecamy zarezerwowanie dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="21db2-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="21db2-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21db2-115">EXAMPLES</span></span>

### <span data-ttu-id="21db2-116">Przykład 1: Inicjowanie grupy administratorów dla serwera</span><span class="sxs-lookup"><span data-stu-id="21db2-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="21db2-117">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="21db2-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="21db2-118">Ten serwer jest skojarzony z grupą ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="21db2-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="21db2-119">Przykład 2: udostępnianie Użytkownikowi administratora dla serwera</span><span class="sxs-lookup"><span data-stu-id="21db2-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="21db2-120">To polecenie inicjuje użytkownikowi usługi Azure AD rolę administratora dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="21db2-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="21db2-121">Przykład 3: Inicjowanie obsługi administracyjnej grupy administratorów przez określenie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="21db2-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="21db2-122">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="21db2-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="21db2-123">W poleceniu określono identyfikator parametru *objectid* .</span><span class="sxs-lookup"><span data-stu-id="21db2-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="21db2-124">Zapewnia to, że polecenie powiedzie się, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="21db2-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="21db2-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21db2-125">PARAMETERS</span></span>

### <span data-ttu-id="21db2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21db2-126">-DefaultProfile</span></span>
<span data-ttu-id="21db2-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21db2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21db2-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21db2-128">-DisplayName</span></span>
<span data-ttu-id="21db2-129">Określa nazwę wyświetlaną administratora usługi Azure AD, która jest zarezerwą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21db2-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="21db2-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="21db2-130">-ObjectId</span></span>
<span data-ttu-id="21db2-131">Określa unikatowy identyfikator administratora usługi Azure AD, który jest zawarty w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21db2-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="21db2-132">Jeśli nazwa wyświetlana nie jest unikatowa, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="21db2-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21db2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21db2-133">-ResourceGroupName</span></span>
<span data-ttu-id="21db2-134">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="21db2-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="21db2-135">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="21db2-135">-ServerName</span></span>
<span data-ttu-id="21db2-136">Określa nazwę serwera SQL, dla którego ten aplet polecenia zainicjuje administrator.</span><span class="sxs-lookup"><span data-stu-id="21db2-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="21db2-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21db2-137">-Confirm</span></span>
<span data-ttu-id="21db2-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21db2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21db2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21db2-139">-WhatIf</span></span>
<span data-ttu-id="21db2-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21db2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21db2-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21db2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21db2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21db2-142">CommonParameters</span></span>
<span data-ttu-id="21db2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21db2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21db2-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21db2-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21db2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21db2-145">INPUTS</span></span>

### <span data-ttu-id="21db2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="21db2-146">System.String</span></span>

### <span data-ttu-id="21db2-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="21db2-147">System.Guid</span></span>

## <span data-ttu-id="21db2-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21db2-148">OUTPUTS</span></span>

### <span data-ttu-id="21db2-149">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="21db2-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="21db2-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21db2-150">NOTES</span></span>

## <span data-ttu-id="21db2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21db2-151">RELATED LINKS</span></span>

[<span data-ttu-id="21db2-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21db2-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="21db2-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="21db2-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="21db2-154">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="21db2-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

