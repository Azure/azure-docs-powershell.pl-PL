---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717300"
---
# <span data-ttu-id="a59eb-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a59eb-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="a59eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a59eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a59eb-103">Tworzy serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a59eb-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a59eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a59eb-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a59eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a59eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a59eb-106">Polecenie cmdlet **New-AzureRmSqlServer** umożliwia utworzenie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a59eb-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="a59eb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a59eb-107">EXAMPLES</span></span>

### <span data-ttu-id="a59eb-108">Przykład 1. Tworzenie nowego serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a59eb-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="a59eb-109">To polecenie tworzy serwer bazy danych SQL Azure w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="a59eb-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="a59eb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a59eb-110">PARAMETERS</span></span>

### <span data-ttu-id="a59eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a59eb-111">-AsJob</span></span>
<span data-ttu-id="a59eb-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a59eb-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="a59eb-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a59eb-113">-AssignIdentity</span></span>
<span data-ttu-id="a59eb-114">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a59eb-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a59eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59eb-115">-DefaultProfile</span></span>
<span data-ttu-id="a59eb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a59eb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a59eb-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a59eb-117">-Location</span></span>
<span data-ttu-id="a59eb-118">Określa lokalizację centrum danych, w którym to polecenie cmdlet tworzy serwer.</span><span class="sxs-lookup"><span data-stu-id="a59eb-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="a59eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a59eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="a59eb-120">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisze serwerowi.</span><span class="sxs-lookup"><span data-stu-id="a59eb-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="a59eb-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a59eb-121">-ServerName</span></span>
<span data-ttu-id="a59eb-122">Określa nazwę nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="a59eb-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a59eb-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a59eb-123">-ServerVersion</span></span>
<span data-ttu-id="a59eb-124">Określa wersję nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="a59eb-124">Specifies the version of the new server.</span></span> <span data-ttu-id="a59eb-125">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="a59eb-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="a59eb-126">Określ 2,0, aby utworzyć serwer w wersji 11 lub 12,0 w celu utworzenia serwera w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="a59eb-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="a59eb-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="a59eb-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="a59eb-128">Określa poświadczenia administratora serwera bazy danych SQL dla nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="a59eb-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="a59eb-129">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="a59eb-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="a59eb-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a59eb-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a59eb-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="a59eb-131">-Tags</span></span>
<span data-ttu-id="a59eb-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a59eb-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a59eb-133">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a59eb-133">For example:</span></span>

<span data-ttu-id="a59eb-134">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a59eb-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a59eb-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a59eb-135">-Confirm</span></span>
<span data-ttu-id="a59eb-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a59eb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a59eb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a59eb-137">-WhatIf</span></span>
<span data-ttu-id="a59eb-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a59eb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a59eb-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a59eb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a59eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59eb-140">CommonParameters</span></span>
<span data-ttu-id="a59eb-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a59eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59eb-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59eb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59eb-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a59eb-143">INPUTS</span></span>

### <span data-ttu-id="a59eb-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a59eb-144">None</span></span>
<span data-ttu-id="a59eb-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a59eb-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a59eb-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a59eb-146">OUTPUTS</span></span>

### <span data-ttu-id="a59eb-147">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a59eb-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a59eb-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a59eb-148">NOTES</span></span>

## <span data-ttu-id="a59eb-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a59eb-149">RELATED LINKS</span></span>

[<span data-ttu-id="a59eb-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a59eb-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="a59eb-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a59eb-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="a59eb-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a59eb-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="a59eb-153">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a59eb-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a59eb-154">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a59eb-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
