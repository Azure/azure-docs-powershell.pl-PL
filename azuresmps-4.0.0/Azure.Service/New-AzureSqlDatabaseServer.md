---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054937"
---
# <span data-ttu-id="4489d-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4489d-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="4489d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4489d-102">SYNOPSIS</span></span>
<span data-ttu-id="4489d-103">Tworzy serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4489d-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="4489d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4489d-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4489d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4489d-105">DESCRIPTION</span></span>
<span data-ttu-id="4489d-106">Polecenie cmdlet **New-AzureSqlDatabaseServer** tworzy wystąpienie serwera bazy danych SQL Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4489d-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="4489d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4489d-107">EXAMPLES</span></span>

### <span data-ttu-id="4489d-108">Przykład 1: Tworzenie serwera</span><span class="sxs-lookup"><span data-stu-id="4489d-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="4489d-109">To polecenie tworzy serwer bazy danych SQL Azure w wersji 11.</span><span class="sxs-lookup"><span data-stu-id="4489d-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="4489d-110">Przykład 2: Tworzenie serwera w wersji 12</span><span class="sxs-lookup"><span data-stu-id="4489d-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="4489d-111">To polecenie tworzy serwer w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="4489d-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="4489d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4489d-112">PARAMETERS</span></span>

### <span data-ttu-id="4489d-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="4489d-113">-AdministratorLogin</span></span>
<span data-ttu-id="4489d-114">Określa nazwę konta administratora dla nowego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4489d-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4489d-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="4489d-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="4489d-116">Określa hasło konta administratora dla serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4489d-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="4489d-117">Musisz określić silne hasło.</span><span class="sxs-lookup"><span data-stu-id="4489d-117">You must specify a strong password.</span></span>
<span data-ttu-id="4489d-118">Aby uzyskać więcej informacji, zobacz [silne hasła](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) w witrynie Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="4489d-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4489d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4489d-119">-Force</span></span>
<span data-ttu-id="4489d-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4489d-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4489d-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4489d-121">-Location</span></span>
<span data-ttu-id="4489d-122">Określa lokalizację centrum danych, w którym to polecenie cmdlet tworzy serwer.</span><span class="sxs-lookup"><span data-stu-id="4489d-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="4489d-123">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) w bibliotece platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="4489d-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4489d-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="4489d-124">-Profile</span></span>
<span data-ttu-id="4489d-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4489d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4489d-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4489d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4489d-127">-Version</span><span class="sxs-lookup"><span data-stu-id="4489d-127">-Version</span></span>
<span data-ttu-id="4489d-128">Określa wersję nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="4489d-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="4489d-129">Prawidłowe wartości: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="4489d-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4489d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4489d-130">-Confirm</span></span>
<span data-ttu-id="4489d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4489d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4489d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4489d-132">-WhatIf</span></span>
<span data-ttu-id="4489d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4489d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4489d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4489d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4489d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4489d-135">CommonParameters</span></span>
<span data-ttu-id="4489d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4489d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4489d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4489d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4489d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4489d-138">INPUTS</span></span>

## <span data-ttu-id="4489d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4489d-139">OUTPUTS</span></span>

### <span data-ttu-id="4489d-140">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="4489d-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="4489d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4489d-141">NOTES</span></span>

## <span data-ttu-id="4489d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4489d-142">RELATED LINKS</span></span>

[<span data-ttu-id="4489d-143">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4489d-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4489d-144">Tworzenie serwera</span><span class="sxs-lookup"><span data-stu-id="4489d-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="4489d-145">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4489d-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4489d-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4489d-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="4489d-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4489d-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="4489d-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4489d-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


