---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548280"
---
# <span data-ttu-id="30c4c-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="30c4c-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="30c4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="30c4c-103">Inicjuje obsługę administracyjną administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30c4c-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30c4c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c4c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="30c4c-106">Polecenie cmdlet **Set-AzureRmSqlServerActiveDirectoryAdministrator** inicjuje administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="30c4c-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="30c4c-107">Możesz dostarczać tylko jednego administratora naraz.</span><span class="sxs-lookup"><span data-stu-id="30c4c-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="30c4c-108">W przypadku administratora programu SQL Server można zainicjować obsługę następujących członków usługi Azure AD:</span><span class="sxs-lookup"><span data-stu-id="30c4c-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="30c4c-109">Natywni członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="30c4c-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="30c4c-110">Federacyjny członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="30c4c-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="30c4c-111">Zaimportowani członkowie z innych reklam usługi Azure, którzy są członkami macierzystymi lub federacyjnymi</span><span class="sxs-lookup"><span data-stu-id="30c4c-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="30c4c-112">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="30c4c-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="30c4c-113">Konta Microsoft, takie jak te w domenach usługi Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="30c4c-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="30c4c-114">Inne konta Gości, takie jak te w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="30c4c-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="30c4c-115">Zalecamy zarezerwowanie dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="30c4c-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="30c4c-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30c4c-116">EXAMPLES</span></span>

### <span data-ttu-id="30c4c-117">Przykład 1: Inicjowanie grupy administratorów dla serwera</span><span class="sxs-lookup"><span data-stu-id="30c4c-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="30c4c-118">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="30c4c-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="30c4c-119">Ten serwer jest skojarzony z grupą ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="30c4c-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="30c4c-120">Przykład 2: udostępnianie Użytkownikowi administratora dla serwera</span><span class="sxs-lookup"><span data-stu-id="30c4c-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="30c4c-121">To polecenie inicjuje użytkownikowi usługi Azure AD rolę administratora dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="30c4c-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="30c4c-122">Przykład 3: Inicjowanie obsługi administracyjnej grupy administratorów przez określenie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="30c4c-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="30c4c-123">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="30c4c-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="30c4c-124">W poleceniu określono identyfikator parametru *objectid* .</span><span class="sxs-lookup"><span data-stu-id="30c4c-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="30c4c-125">Zapewnia to, że polecenie powiedzie się, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="30c4c-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="30c4c-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30c4c-126">PARAMETERS</span></span>

### <span data-ttu-id="30c4c-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="30c4c-127">-DisplayName</span></span>
<span data-ttu-id="30c4c-128">Określa nazwę wyświetlaną administratora usługi Azure AD, która jest zarezerwą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c4c-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="30c4c-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30c4c-129">-ObjectId</span></span>
<span data-ttu-id="30c4c-130">Określa unikatowy identyfikator administratora usługi Azure AD, który jest zawarty w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c4c-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="30c4c-131">Jeśli nazwa wyświetlana nie jest unikatowa, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="30c4c-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="30c4c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c4c-132">-ResourceGroupName</span></span>
<span data-ttu-id="30c4c-133">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="30c4c-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="30c4c-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="30c4c-134">-ServerName</span></span>
<span data-ttu-id="30c4c-135">Określa nazwę serwera SQL, dla którego ten aplet polecenia zainicjuje administrator.</span><span class="sxs-lookup"><span data-stu-id="30c4c-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="30c4c-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30c4c-136">-Confirm</span></span>
<span data-ttu-id="30c4c-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c4c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c4c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c4c-138">-WhatIf</span></span>
<span data-ttu-id="30c4c-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c4c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c4c-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30c4c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c4c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c4c-141">-DefaultProfile</span></span>
<span data-ttu-id="30c4c-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30c4c-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c4c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c4c-143">CommonParameters</span></span>
<span data-ttu-id="30c4c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c4c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c4c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c4c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c4c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30c4c-146">INPUTS</span></span>

## <span data-ttu-id="30c4c-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30c4c-147">OUTPUTS</span></span>

### <span data-ttu-id="30c4c-148">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="30c4c-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="30c4c-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30c4c-149">NOTES</span></span>

## <span data-ttu-id="30c4c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30c4c-150">RELATED LINKS</span></span>

[<span data-ttu-id="30c4c-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="30c4c-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="30c4c-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="30c4c-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="30c4c-153">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="30c4c-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


