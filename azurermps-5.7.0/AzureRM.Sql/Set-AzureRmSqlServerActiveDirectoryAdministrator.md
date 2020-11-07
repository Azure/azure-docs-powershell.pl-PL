---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 43dbbe6ca4f24e98bcfc45703c387ccb5fb4db03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716978"
---
# <span data-ttu-id="4c730-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4c730-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="4c730-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c730-102">SYNOPSIS</span></span>
<span data-ttu-id="4c730-103">Inicjuje obsługę administracyjną administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c730-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c730-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c730-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c730-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c730-105">DESCRIPTION</span></span>
<span data-ttu-id="4c730-106">Polecenie cmdlet **Set-AzureRmSqlServerActiveDirectoryAdministrator** inicjuje administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4c730-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="4c730-107">Możesz dostarczać tylko jednego administratora naraz.</span><span class="sxs-lookup"><span data-stu-id="4c730-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="4c730-108">W przypadku administratora programu SQL Server można zainicjować obsługę następujących członków usługi Azure AD:</span><span class="sxs-lookup"><span data-stu-id="4c730-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="4c730-109">Natywni członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="4c730-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="4c730-110">Federacyjny członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="4c730-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="4c730-111">Zaimportowani członkowie z innych reklam usługi Azure, którzy są członkami macierzystymi lub federacyjnymi</span><span class="sxs-lookup"><span data-stu-id="4c730-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="4c730-112">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="4c730-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="4c730-113">Konta Microsoft, takie jak te w domenach usługi Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="4c730-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="4c730-114">Inne konta Gości, takie jak te w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="4c730-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="4c730-115">Zalecamy zarezerwowanie dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="4c730-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="4c730-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c730-116">EXAMPLES</span></span>

### <span data-ttu-id="4c730-117">Przykład 1: Inicjowanie grupy administratorów dla serwera</span><span class="sxs-lookup"><span data-stu-id="4c730-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="4c730-118">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4c730-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="4c730-119">Ten serwer jest skojarzony z grupą ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4c730-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="4c730-120">Przykład 2: udostępnianie Użytkownikowi administratora dla serwera</span><span class="sxs-lookup"><span data-stu-id="4c730-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="4c730-121">To polecenie inicjuje użytkownikowi usługi Azure AD rolę administratora dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4c730-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="4c730-122">Przykład 3: Inicjowanie obsługi administracyjnej grupy administratorów przez określenie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="4c730-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="4c730-123">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4c730-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="4c730-124">W poleceniu określono identyfikator parametru *objectid* .</span><span class="sxs-lookup"><span data-stu-id="4c730-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="4c730-125">Zapewnia to, że polecenie powiedzie się, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="4c730-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="4c730-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c730-126">PARAMETERS</span></span>

### <span data-ttu-id="4c730-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c730-127">-DefaultProfile</span></span>
<span data-ttu-id="4c730-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4c730-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c730-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c730-129">-DisplayName</span></span>
<span data-ttu-id="4c730-130">Określa nazwę wyświetlaną administratora usługi Azure AD, która jest zarezerwą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c730-130">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c730-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4c730-131">-ObjectId</span></span>
<span data-ttu-id="4c730-132">Określa unikatowy identyfikator administratora usługi Azure AD, który jest zawarty w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c730-132">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="4c730-133">Jeśli nazwa wyświetlana nie jest unikatowa, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="4c730-133">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c730-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c730-134">-ResourceGroupName</span></span>
<span data-ttu-id="4c730-135">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="4c730-135">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4c730-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4c730-136">-ServerName</span></span>
<span data-ttu-id="4c730-137">Określa nazwę serwera SQL, dla którego ten aplet polecenia zainicjuje administrator.</span><span class="sxs-lookup"><span data-stu-id="4c730-137">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="4c730-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c730-138">-Confirm</span></span>
<span data-ttu-id="4c730-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c730-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c730-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c730-140">-WhatIf</span></span>
<span data-ttu-id="4c730-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c730-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c730-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c730-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c730-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c730-143">CommonParameters</span></span>
<span data-ttu-id="4c730-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c730-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c730-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c730-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c730-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c730-146">INPUTS</span></span>

### <span data-ttu-id="4c730-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4c730-147">None</span></span>
<span data-ttu-id="4c730-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4c730-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c730-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c730-149">OUTPUTS</span></span>

### <span data-ttu-id="4c730-150">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="4c730-150">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="4c730-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c730-151">NOTES</span></span>

## <span data-ttu-id="4c730-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c730-152">RELATED LINKS</span></span>

[<span data-ttu-id="4c730-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4c730-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4c730-154">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4c730-154">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4c730-155">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4c730-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


