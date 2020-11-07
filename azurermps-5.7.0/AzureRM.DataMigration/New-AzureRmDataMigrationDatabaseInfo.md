---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718929"
---
# <span data-ttu-id="efcfc-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="efcfc-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="efcfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="efcfc-103">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="efcfc-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efcfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efcfc-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="efcfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="efcfc-105">DESCRIPTION</span></span>
<span data-ttu-id="efcfc-106">Polecenie cmdlet New-AzureRmDataMigrationDatabaseInfo tworzy obiekt DatabaseInfo, który określa wystąpienie źródłowej bazy danych, do której należy przeprowadzić migrację.</span><span class="sxs-lookup"><span data-stu-id="efcfc-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="efcfc-107">Nazwa bazy danych jest pobierana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="efcfc-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="efcfc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efcfc-108">EXAMPLES</span></span>

### <span data-ttu-id="efcfc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efcfc-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="efcfc-110">W powyższym przykładzie tworzony jest nowy obiekt DatabaseInfo dla źródłowej **AdventureWorks2016** bazy danych.</span><span class="sxs-lookup"><span data-stu-id="efcfc-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="efcfc-111">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="efcfc-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="efcfc-112">Możesz potwierdzić stan logowania, korzystając z polecenia cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="efcfc-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="efcfc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efcfc-113">PARAMETERS</span></span>

### <span data-ttu-id="efcfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcfc-114">-DefaultProfile</span></span>
<span data-ttu-id="efcfc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="efcfc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="efcfc-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efcfc-116">-Confirm</span></span>
<span data-ttu-id="efcfc-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efcfc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efcfc-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="efcfc-118">-SourceDatabaseName</span></span>
<span data-ttu-id="efcfc-119">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="efcfc-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcfc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efcfc-120">-WhatIf</span></span>
<span data-ttu-id="efcfc-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efcfc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efcfc-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="efcfc-122">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="efcfc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efcfc-123">INPUTS</span></span>

### <span data-ttu-id="efcfc-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="efcfc-124">None</span></span>


## <span data-ttu-id="efcfc-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efcfc-125">OUTPUTS</span></span>

### <span data-ttu-id="efcfc-126">Microsoft. Azure. Management. datamigration. MODELES. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="efcfc-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="efcfc-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efcfc-127">NOTES</span></span>

## <span data-ttu-id="efcfc-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efcfc-128">RELATED LINKS</span></span>


