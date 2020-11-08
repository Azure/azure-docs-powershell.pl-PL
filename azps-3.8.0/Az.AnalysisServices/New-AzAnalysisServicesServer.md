---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050938"
---
# <span data-ttu-id="8b00d-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8b00d-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8b00d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b00d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b00d-103">Tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="8b00d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b00d-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b00d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b00d-105">DESCRIPTION</span></span>
<span data-ttu-id="8b00d-106">Polecenie cmdlet New-AzAnalysisServicesServer tworzy nowy serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="8b00d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b00d-107">EXAMPLES</span></span>

### <span data-ttu-id="8b00d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b00d-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="8b00d-109">Tworzy serwer o nazwie TestServer w regionie Azure w Stanach Zjednoczonych i w testresourcegroup grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b00d-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="8b00d-110">Poziom wersji SKU dla serwera to S1.</span><span class="sxs-lookup"><span data-stu-id="8b00d-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="8b00d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b00d-111">PARAMETERS</span></span>

### <span data-ttu-id="8b00d-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="8b00d-112">-Administrator</span></span>
<span data-ttu-id="8b00d-113">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8b00d-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="8b00d-114">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8b00d-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="8b00d-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="8b00d-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="8b00d-116">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="8b00d-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="8b00d-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="8b00d-118">Domyślny tryb połączenia serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="8b00d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b00d-119">-DefaultProfile</span></span>
<span data-ttu-id="8b00d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b00d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b00d-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="8b00d-121">-FirewallConfig</span></span>
<span data-ttu-id="8b00d-122">Konfiguracja zapory serwera analiz</span><span class="sxs-lookup"><span data-stu-id="8b00d-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="8b00d-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8b00d-123">-GatewayResourceId</span></span>
<span data-ttu-id="8b00d-124">Identyfikator zasobu bramy skojarzony z serwerem analizy</span><span class="sxs-lookup"><span data-stu-id="8b00d-124">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="8b00d-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b00d-125">-Location</span></span>
<span data-ttu-id="8b00d-126">Obszar platformy Azure, w którym znajduje się serwer usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="8b00d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b00d-127">-Name</span></span>
<span data-ttu-id="8b00d-128">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8b00d-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8b00d-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="8b00d-130">Liczba replik tylko do odczytu serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8b00d-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="8b00d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b00d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b00d-132">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="8b00d-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8b00d-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b00d-133">-Sku</span></span>
<span data-ttu-id="8b00d-134">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="8b00d-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="8b00d-135">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="8b00d-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="8b00d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b00d-136">-Tag</span></span>
<span data-ttu-id="8b00d-137">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8b00d-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="8b00d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b00d-138">-Confirm</span></span>
<span data-ttu-id="8b00d-139">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="8b00d-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8b00d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b00d-140">-WhatIf</span></span>
<span data-ttu-id="8b00d-141">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8b00d-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8b00d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b00d-142">CommonParameters</span></span>
<span data-ttu-id="8b00d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b00d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b00d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b00d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b00d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b00d-145">INPUTS</span></span>

### <span data-ttu-id="8b00d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8b00d-146">System.String</span></span>

### <span data-ttu-id="8b00d-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b00d-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b00d-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8b00d-148">System.Int32</span></span>

### <span data-ttu-id="8b00d-149">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="8b00d-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="8b00d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b00d-150">OUTPUTS</span></span>

### <span data-ttu-id="8b00d-151">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8b00d-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8b00d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b00d-152">NOTES</span></span>
<span data-ttu-id="8b00d-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="8b00d-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="8b00d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b00d-154">RELATED LINKS</span></span>

[<span data-ttu-id="8b00d-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8b00d-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="8b00d-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8b00d-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
