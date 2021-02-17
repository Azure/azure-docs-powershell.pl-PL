---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243251"
---
# <span data-ttu-id="05458-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="05458-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="05458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05458-102">SYNOPSIS</span></span>
<span data-ttu-id="05458-103">Inistruje administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05458-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="05458-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05458-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05458-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="05458-105">DESCRIPTION</span></span>
<span data-ttu-id="05458-106">Polecenie **cmdlet Set-AzSqlServerActiveDirectoryAdministrator** inicjałuje administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="05458-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="05458-107">W jednej chwili możesz korzystać z obsługi administracyjnej tylko jednego administratora.</span><span class="sxs-lookup"><span data-stu-id="05458-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="05458-108">Oto członkowie usługi Azure AD, których można używać jako administrator programu SQL Server:</span><span class="sxs-lookup"><span data-stu-id="05458-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="05458-109">Natywne członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="05458-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="05458-110">Federowani członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="05458-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="05458-111">Zaimportowani członkowie z innych identyfikatorów Azure ADS, którzy są członkami natywnymi lub federtywnymi</span><span class="sxs-lookup"><span data-stu-id="05458-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="05458-112">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń konta Microsoft, takie jak konta Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="05458-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="05458-113">Inne konta gości, na przykład konta w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="05458-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="05458-114">Zalecamy inicjowanie obsługi dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="05458-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="05458-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05458-115">EXAMPLES</span></span>

### <span data-ttu-id="05458-116">Przykład 1. Inicjowanie obsługi grupy administratorów dla serwera</span><span class="sxs-lookup"><span data-stu-id="05458-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="05458-117">To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="05458-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="05458-118">Ten serwer jest skojarzony z grupą zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="05458-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="05458-119">Przykład 2. Inicjowanie obsługi administracyjnej użytkownika administratora serwera</span><span class="sxs-lookup"><span data-stu-id="05458-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="05458-120">To polecenie iniekuje użytkownika usługi Azure AD jako administratora serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="05458-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="05458-121">Przykład 3. Inicjowanie obsługi grupy administratorów przez podanie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="05458-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="05458-122">To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="05458-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="05458-123">To polecenie określa identyfikator *parametru ObjectId.*</span><span class="sxs-lookup"><span data-stu-id="05458-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="05458-124">Dzięki temu można mieć pewność, że polecenie zakończy się powodzeniem, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="05458-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="05458-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05458-125">PARAMETERS</span></span>

### <span data-ttu-id="05458-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05458-126">-DefaultProfile</span></span>
<span data-ttu-id="05458-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="05458-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05458-128">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="05458-128">-DisplayName</span></span>
<span data-ttu-id="05458-129">Określa nazwę wyświetlaną administratora usługi Azure AD, który ma inicjuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05458-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="05458-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="05458-130">-ObjectId</span></span>
<span data-ttu-id="05458-131">Określa unikatowy identyfikator administratora usługi Azure AD, który ma inicjuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05458-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="05458-132">Jeśli nazwa wyświetlana nie jest unikatowa, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="05458-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="05458-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05458-133">-ResourceGroupName</span></span>
<span data-ttu-id="05458-134">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="05458-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="05458-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05458-135">-ServerName</span></span>
<span data-ttu-id="05458-136">Określa nazwę serwera SQL, dla którego to polecenie cmdlet iniekuje administratora.</span><span class="sxs-lookup"><span data-stu-id="05458-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="05458-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05458-137">-Confirm</span></span>
<span data-ttu-id="05458-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05458-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05458-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05458-139">-WhatIf</span></span>
<span data-ttu-id="05458-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05458-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05458-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05458-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05458-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05458-142">CommonParameters</span></span>
<span data-ttu-id="05458-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05458-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05458-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05458-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05458-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05458-145">INPUTS</span></span>

### <span data-ttu-id="05458-146">System.String</span><span class="sxs-lookup"><span data-stu-id="05458-146">System.String</span></span>

### <span data-ttu-id="05458-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="05458-147">System.Guid</span></span>

## <span data-ttu-id="05458-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05458-148">OUTPUTS</span></span>

### <span data-ttu-id="05458-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="05458-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="05458-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05458-150">NOTES</span></span>

## <span data-ttu-id="05458-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05458-151">RELATED LINKS</span></span>

[<span data-ttu-id="05458-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="05458-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="05458-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="05458-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="05458-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="05458-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="05458-155">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="05458-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


