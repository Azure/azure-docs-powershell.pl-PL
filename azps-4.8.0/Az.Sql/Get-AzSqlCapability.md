---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222236"
---
# <span data-ttu-id="110bd-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="110bd-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="110bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="110bd-102">SYNOPSIS</span></span>
<span data-ttu-id="110bd-103">Pobiera funkcje bazy danych SQL dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="110bd-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="110bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="110bd-104">SYNTAX</span></span>

### <span data-ttu-id="110bd-105">FilterResults (domyślny)</span><span class="sxs-lookup"><span data-stu-id="110bd-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="110bd-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="110bd-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="110bd-107">DESCRIPTION</span></span>
<span data-ttu-id="110bd-108">Polecenie cmdlet **Get-AzSqlCapability** pobiera funkcje bazy danych SQL Azure dostępne w bieżącej subskrypcji regionu.</span><span class="sxs-lookup"><span data-stu-id="110bd-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="110bd-109">Jeśli określisz parametry *ServerVersionName* , *Edition* lub *serviceobiektywname* , to polecenie cmdlet zwróci określone wartości i ich poprzedniki.</span><span class="sxs-lookup"><span data-stu-id="110bd-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="110bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="110bd-110">EXAMPLES</span></span>

### <span data-ttu-id="110bd-111">Przykład 1: Uzyskaj możliwości dla bieżącej subskrypcji w regionie</span><span class="sxs-lookup"><span data-stu-id="110bd-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="110bd-112">To polecenie zwraca możliwości wystąpienia bazy danych SQL w bieżącej subskrypcji dla centralnego regionu w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="110bd-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="110bd-113">Przykład 2: uzyskiwanie funkcji domyślnych dla bieżącej subskrypcji dla regionu</span><span class="sxs-lookup"><span data-stu-id="110bd-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="110bd-114">To polecenie zwraca domyślne funkcje baz danych SQL w bieżącej subskrypcji w obszarze Centrala Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="110bd-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="110bd-115">Przykład 3: uzyskiwanie szczegółowych informacji dotyczących celu świadczenia usługi</span><span class="sxs-lookup"><span data-stu-id="110bd-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="110bd-116">To polecenie pobiera domyślne funkcje baz danych SQL dla określonego celu usługi w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="110bd-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="110bd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="110bd-117">PARAMETERS</span></span>

### <span data-ttu-id="110bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110bd-118">-DefaultProfile</span></span>
<span data-ttu-id="110bd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="110bd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="110bd-120">-Ustawienia domyślne</span><span class="sxs-lookup"><span data-stu-id="110bd-120">-Defaults</span></span>
<span data-ttu-id="110bd-121">Wskazuje, że w tym poleceniu cmdlet są pobierane tylko wartości domyślne.</span><span class="sxs-lookup"><span data-stu-id="110bd-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110bd-122">-Wydanie</span><span class="sxs-lookup"><span data-stu-id="110bd-122">-EditionName</span></span>
<span data-ttu-id="110bd-123">Określa nazwę wersji bazy danych, w której to polecenie cmdlet pobiera funkcje.</span><span class="sxs-lookup"><span data-stu-id="110bd-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110bd-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="110bd-124">-LocationName</span></span>
<span data-ttu-id="110bd-125">Określa nazwę lokalizacji, w której ten aplet polecenia pobiera funkcje.</span><span class="sxs-lookup"><span data-stu-id="110bd-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="110bd-126">Aby uzyskać więcej informacji, zobacz regiony platformy Azure http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="110bd-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="110bd-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="110bd-127">-ServerVersionName</span></span>
<span data-ttu-id="110bd-128">Określa nazwę wersji serwera, w której ten aplet polecenia pobiera funkcje.</span><span class="sxs-lookup"><span data-stu-id="110bd-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110bd-129">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="110bd-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="110bd-130">Określa nazwę celu usługi, dla którego to polecenie cmdlet pobiera funkcje.</span><span class="sxs-lookup"><span data-stu-id="110bd-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110bd-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="110bd-131">-Confirm</span></span>
<span data-ttu-id="110bd-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="110bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110bd-133">-WhatIf</span></span>
<span data-ttu-id="110bd-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="110bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="110bd-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="110bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110bd-136">CommonParameters</span></span>
<span data-ttu-id="110bd-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110bd-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="110bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110bd-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="110bd-139">INPUTS</span></span>

### <span data-ttu-id="110bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="110bd-140">System.String</span></span>

## <span data-ttu-id="110bd-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="110bd-141">OUTPUTS</span></span>

### <span data-ttu-id="110bd-142">Microsoft.Azure.Commands.Sql.Location_Capabilities. model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="110bd-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="110bd-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="110bd-143">NOTES</span></span>

## <span data-ttu-id="110bd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="110bd-144">RELATED LINKS</span></span>
