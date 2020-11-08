---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054534"
---
# <span data-ttu-id="d09f6-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="d09f6-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="d09f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d09f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d09f6-103">Umożliwia pobieranie celów usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d09f6-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="d09f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d09f6-104">SYNTAX</span></span>

### <span data-ttu-id="d09f6-105">ByConnectionContext (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d09f6-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d09f6-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="d09f6-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d09f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d09f6-107">DESCRIPTION</span></span>
<span data-ttu-id="d09f6-108">Polecenie cmdlet **Get-AzureSqlDatabaseServiceObjective** umożliwia realizację celów usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d09f6-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="d09f6-109">Cele usługi są określane jako poziomy wydajności.</span><span class="sxs-lookup"><span data-stu-id="d09f6-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="d09f6-110">Jeśli nie określisz celu usługi, to polecenie cmdlet zwróci wszystkie ważne cele usługi dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="d09f6-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="d09f6-111">To polecenie cmdlet dotyczy warstw usług podstawowych, standardowych i Premium.</span><span class="sxs-lookup"><span data-stu-id="d09f6-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="d09f6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d09f6-112">EXAMPLES</span></span>

### <span data-ttu-id="d09f6-113">Przykład 1: uzyskiwanie wszystkich celów usługi za pomocą kontekstu połączenia</span><span class="sxs-lookup"><span data-stu-id="d09f6-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="d09f6-114">To polecenie pobiera wszystkie cele usługi dla serwera, który $Context określał kontekst połączenia.</span><span class="sxs-lookup"><span data-stu-id="d09f6-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="d09f6-115">Przykład 2: uzyskiwanie wszystkich celów usługi przy użyciu nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="d09f6-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="d09f6-116">To polecenie pobiera wszystkie cele usługi dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="d09f6-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="d09f6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d09f6-117">PARAMETERS</span></span>

### <span data-ttu-id="d09f6-118">-Context</span><span class="sxs-lookup"><span data-stu-id="d09f6-118">-Context</span></span>
<span data-ttu-id="d09f6-119">Określa kontekst połączenia serwera.</span><span class="sxs-lookup"><span data-stu-id="d09f6-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09f6-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="d09f6-120">-Profile</span></span>
<span data-ttu-id="d09f6-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d09f6-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d09f6-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d09f6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09f6-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d09f6-123">-ServerName</span></span>
<span data-ttu-id="d09f6-124">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="d09f6-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d09f6-125">-Servicesprzeciw</span><span class="sxs-lookup"><span data-stu-id="d09f6-125">-ServiceObjective</span></span>
<span data-ttu-id="d09f6-126">Określa obiekt reprezentujący cel usługi, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d09f6-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="d09f6-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d09f6-127">Valid values are:</span></span> 

- <span data-ttu-id="d09f6-128">Podstawowe: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="d09f6-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="d09f6-129">Standardowo (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="d09f6-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="d09f6-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="d09f6-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="d09f6-131">Standardowo (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="d09f6-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="d09f6-132">\* Standard (S3): 789681b8-Ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="d09f6-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="d09f6-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="d09f6-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="d09f6-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="d09f6-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="d09f6-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="d09f6-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="d09f6-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="d09f6-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="d09f6-137">\* Standard (S3) jest częścią najnowszej aktualizacji bazy danych SQL V12 (wersja Preview).</span><span class="sxs-lookup"><span data-stu-id="d09f6-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="d09f6-138">Aby uzyskać więcej informacji, zobacz [co nowego w usłudze Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) w bibliotece platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d09f6-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09f6-139">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="d09f6-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="d09f6-140">Określa nazwę celu usługi, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="d09f6-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="d09f6-141">Prawidłowe wartości to: Basic, S0, S1, S2, S3, P1, P2 i P3.</span><span class="sxs-lookup"><span data-stu-id="d09f6-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09f6-142">CommonParameters</span></span>
<span data-ttu-id="d09f6-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09f6-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09f6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09f6-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d09f6-145">INPUTS</span></span>

### <span data-ttu-id="d09f6-146">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. serviceobject</span><span class="sxs-lookup"><span data-stu-id="d09f6-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="d09f6-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d09f6-147">OUTPUTS</span></span>

### <span data-ttu-id="d09f6-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="d09f6-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="d09f6-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d09f6-149">NOTES</span></span>

## <span data-ttu-id="d09f6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d09f6-150">RELATED LINKS</span></span>

[<span data-ttu-id="d09f6-151">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d09f6-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="d09f6-152">Uzyskiwanie celu na poziomie usługi</span><span class="sxs-lookup"><span data-stu-id="d09f6-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="d09f6-153">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d09f6-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d09f6-154">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="d09f6-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


