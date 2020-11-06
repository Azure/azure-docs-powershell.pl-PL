---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: d8a795cc27a09fe7b23ac2156115d7a52212e3ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547728"
---
# <span data-ttu-id="628fa-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="628fa-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="628fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="628fa-102">SYNOPSIS</span></span>
<span data-ttu-id="628fa-103">Tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="628fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="628fa-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="628fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="628fa-105">DESCRIPTION</span></span>
<span data-ttu-id="628fa-106">Polecenie cmdlet New-AzureRmAnalysisServicesServer tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="628fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="628fa-107">EXAMPLES</span></span>

### <span data-ttu-id="628fa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="628fa-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="628fa-109">Tworzy serwer o nazwie TestServer w regionie Azure w Stanach Zjednoczonych i w testresrourcegroup grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="628fa-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="628fa-110">Poziom wersji SKU dla serwera to S1.</span><span class="sxs-lookup"><span data-stu-id="628fa-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="628fa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="628fa-111">PARAMETERS</span></span>

### <span data-ttu-id="628fa-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="628fa-112">-Administrator</span></span>
<span data-ttu-id="628fa-113">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="628fa-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="628fa-114">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="628fa-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="628fa-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="628fa-116">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="628fa-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="628fa-118">Domyślny tryb połączenia serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628fa-119">-DefaultProfile</span></span>
<span data-ttu-id="628fa-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="628fa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="628fa-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="628fa-121">-FirewallConfig</span></span>
<span data-ttu-id="628fa-122">Konfiguracja zapory serwera analiz</span><span class="sxs-lookup"><span data-stu-id="628fa-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="628fa-123">-GatewayResourceId</span></span>
<span data-ttu-id="628fa-124">Identyfikator zasobu bramy dla assocaite do serwera analizy</span><span class="sxs-lookup"><span data-stu-id="628fa-124">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="628fa-125">-Location</span></span>
<span data-ttu-id="628fa-126">Obszar platformy Azure, w którym znajduje się serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="628fa-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="628fa-127">-Name</span></span>
<span data-ttu-id="628fa-128">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="628fa-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="628fa-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="628fa-130">Liczba replik tylko do odczytu serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="628fa-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="628fa-132">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="628fa-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="628fa-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="628fa-133">-Sku</span></span>
<span data-ttu-id="628fa-134">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="628fa-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="628fa-135">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="628fa-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="628fa-136">-Tag</span></span>
<span data-ttu-id="628fa-137">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="628fa-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="628fa-138">-Confirm</span></span>
<span data-ttu-id="628fa-139">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="628fa-139">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628fa-140">-WhatIf</span></span>
<span data-ttu-id="628fa-141">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="628fa-141">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628fa-142">CommonParameters</span></span>
<span data-ttu-id="628fa-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="628fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628fa-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628fa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628fa-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="628fa-145">INPUTS</span></span>

### <span data-ttu-id="628fa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="628fa-146">System.String</span></span>

### <span data-ttu-id="628fa-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="628fa-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="628fa-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="628fa-148">System.Int32</span></span>

### <span data-ttu-id="628fa-149">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="628fa-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="628fa-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="628fa-150">OUTPUTS</span></span>

### <span data-ttu-id="628fa-151">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="628fa-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="628fa-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="628fa-152">NOTES</span></span>
<span data-ttu-id="628fa-153">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="628fa-153">Alias: New-AzureAs</span></span>

## <span data-ttu-id="628fa-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="628fa-154">RELATED LINKS</span></span>

[<span data-ttu-id="628fa-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="628fa-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="628fa-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="628fa-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
