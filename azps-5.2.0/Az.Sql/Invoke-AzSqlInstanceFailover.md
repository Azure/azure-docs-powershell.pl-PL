---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360689"
---
# <span data-ttu-id="fd53f-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="fd53f-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="fd53f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd53f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd53f-103">Praca awaryjna wystąpienia zarządzanego przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fd53f-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="fd53f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd53f-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd53f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd53f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd53f-106">Polecenie cmdlet **Invoke-AzSqlInstanceFailover** w trybie failover wystąpienia zarządzanego SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fd53f-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="fd53f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd53f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd53f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd53f-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="fd53f-109">To polecenie przejdzie w tryb failover replika podstawowa wystąpienia o nazwie "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="fd53f-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="fd53f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd53f-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="fd53f-111">To polecenie przejdzie w tryb failover do czytelnej repliki pomocniczej zarządzanego wystąpienia "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="fd53f-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="fd53f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd53f-112">PARAMETERS</span></span>

### <span data-ttu-id="fd53f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd53f-113">-AsJob</span></span>
<span data-ttu-id="fd53f-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fd53f-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd53f-115">-DefaultProfile</span></span>
<span data-ttu-id="fd53f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd53f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd53f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fd53f-117">-Force</span></span>
<span data-ttu-id="fd53f-118">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="fd53f-118">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd53f-119">-Name</span></span>
<span data-ttu-id="fd53f-120">Nazwa wystąpienia SQL Azure, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="fd53f-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd53f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd53f-121">-PassThru</span></span>
<span data-ttu-id="fd53f-122">Po udanym wykonaniu zwraca wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="fd53f-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="fd53f-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fd53f-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53f-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="fd53f-124">-ReadableSecondary</span></span>
<span data-ttu-id="fd53f-125">Przejmowanie awaryjnej repliki pomocniczej zamiast domyślnej repliki podstawowej</span><span class="sxs-lookup"><span data-stu-id="fd53f-125">Failover the readable secondary replica instead of the default primary replica</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd53f-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd53f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd53f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd53f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd53f-128">-Confirm</span></span>
<span data-ttu-id="fd53f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd53f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd53f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd53f-130">-WhatIf</span></span>
<span data-ttu-id="fd53f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd53f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd53f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd53f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd53f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd53f-133">CommonParameters</span></span>
<span data-ttu-id="fd53f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd53f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd53f-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd53f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd53f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd53f-136">INPUTS</span></span>

### <span data-ttu-id="fd53f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fd53f-137">System.String</span></span>

## <span data-ttu-id="fd53f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd53f-138">OUTPUTS</span></span>

## <span data-ttu-id="fd53f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd53f-139">NOTES</span></span>

## <span data-ttu-id="fd53f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd53f-140">RELATED LINKS</span></span>
