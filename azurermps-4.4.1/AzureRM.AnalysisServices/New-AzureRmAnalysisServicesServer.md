---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525821"
---
# <span data-ttu-id="f7092-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f7092-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f7092-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7092-102">SYNOPSIS</span></span>
<span data-ttu-id="f7092-103">Tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f7092-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7092-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7092-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7092-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7092-105">DESCRIPTION</span></span>
<span data-ttu-id="f7092-106">Polecenie cmdlet New-AzureRmAnalysisServicesServer tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f7092-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="f7092-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7092-107">EXAMPLES</span></span>

### <span data-ttu-id="f7092-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7092-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="f7092-109">Tworzy serwer o nazwie TestServer w regionie Azure w Stanach Zjednoczonych i w testresrourcegroup grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7092-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="f7092-110">Poziom wersji SKU dla serwera to S1.</span><span class="sxs-lookup"><span data-stu-id="f7092-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="f7092-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7092-111">PARAMETERS</span></span>

### <span data-ttu-id="f7092-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="f7092-112">-Administrator</span></span>
<span data-ttu-id="f7092-113">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f7092-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="f7092-114">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f7092-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7092-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f7092-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="f7092-116">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f7092-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7092-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f7092-117">-Location</span></span>
<span data-ttu-id="f7092-118">Obszar platformy Azure, w którym znajduje się serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f7092-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7092-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7092-119">-Name</span></span>
<span data-ttu-id="f7092-120">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f7092-120">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f7092-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7092-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7092-122">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="f7092-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f7092-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="f7092-123">-Sku</span></span>
<span data-ttu-id="f7092-124">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="f7092-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="f7092-125">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="f7092-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7092-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7092-126">-Tag</span></span>
<span data-ttu-id="f7092-127">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f7092-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7092-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7092-128">-Confirm</span></span>
<span data-ttu-id="f7092-129">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="f7092-129">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f7092-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7092-130">-WhatIf</span></span>
<span data-ttu-id="f7092-131">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="f7092-131">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f7092-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7092-132">CommonParameters</span></span>
<span data-ttu-id="f7092-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7092-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7092-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7092-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7092-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7092-135">INPUTS</span></span>

## <span data-ttu-id="f7092-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7092-136">OUTPUTS</span></span>

### <span data-ttu-id="f7092-137">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f7092-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f7092-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7092-138">NOTES</span></span>
<span data-ttu-id="f7092-139">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f7092-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="f7092-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7092-140">RELATED LINKS</span></span>

[<span data-ttu-id="f7092-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f7092-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="f7092-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f7092-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
