---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528150"
---
# <span data-ttu-id="5ddba-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="5ddba-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="5ddba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ddba-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddba-103">Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="5ddba-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ddba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ddba-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="5ddba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ddba-105">DESCRIPTION</span></span>
<span data-ttu-id="5ddba-106">Polecenie cmdlet New-AzureRmDataMigrationConnectionInfo służy do tworzenia nowego obiektu informacji o połączeniu określającego typ serwera dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="5ddba-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="5ddba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ddba-107">EXAMPLES</span></span>

### <span data-ttu-id="5ddba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ddba-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="5ddba-109">W powyższym przykładzie tworzony jest nowy obiekt informacji o połączeniu, który udostępnia parametry SQL jako parametr ServerType.</span><span class="sxs-lookup"><span data-stu-id="5ddba-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="5ddba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ddba-110">PARAMETERS</span></span>

### <span data-ttu-id="5ddba-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ddba-111">-Confirm</span></span>
<span data-ttu-id="5ddba-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ddba-112">Prompts you for confirmation before running the cmdlet.</span></span>

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
### <span data-ttu-id="5ddba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddba-113">-DefaultProfile</span></span>
<span data-ttu-id="5ddba-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ddba-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="5ddba-115">-ServerType</span></span>
<span data-ttu-id="5ddba-116">Wyliczenie opisujące typ serwera, z którym ma zostać nawiązane połączenie.</span><span class="sxs-lookup"><span data-stu-id="5ddba-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="5ddba-117">Obecnie obsługiwane są wartości SQL dla programu SQL Server i SQLDB dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddba-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="5ddba-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="5ddba-118">-AuthType</span></span>
<span data-ttu-id="5ddba-119">Typ uwierzytelniania, który ma być używany do połączeń.</span><span class="sxs-lookup"><span data-stu-id="5ddba-119">Authentication type to use for connection.</span></span> <span data-ttu-id="5ddba-120">Możliwe wartości to sqlauthentication and WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="5ddba-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddba-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5ddba-121">-DataSource</span></span>
<span data-ttu-id="5ddba-122">Serwer address\name, z którym chcesz się połączyć.</span><span class="sxs-lookup"><span data-stu-id="5ddba-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddba-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="5ddba-123">-TrustServerCertificate</span></span>
<span data-ttu-id="5ddba-124">Wartość logiczna wskazująca na zagwarantowanie, że szyfrowanie ma miejsce.</span><span class="sxs-lookup"><span data-stu-id="5ddba-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddba-125">-WhatIf</span></span>
<span data-ttu-id="5ddba-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ddba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ddba-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ddba-127">The cmdlet is not run.</span></span>

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





## <span data-ttu-id="5ddba-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ddba-128">INPUTS</span></span>

### <span data-ttu-id="5ddba-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5ddba-129">None</span></span>


## <span data-ttu-id="5ddba-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ddba-130">OUTPUTS</span></span>

### <span data-ttu-id="5ddba-131">Microsoft. Azure. Management. datamigration. MODELES. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="5ddba-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="5ddba-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ddba-132">NOTES</span></span>

## <span data-ttu-id="5ddba-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ddba-133">RELATED LINKS</span></span>

