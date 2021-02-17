---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176898"
---
# <span data-ttu-id="6b408-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="6b408-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="6b408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b408-102">SYNOPSIS</span></span>
<span data-ttu-id="6b408-103">Failovers an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="6b408-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6b408-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b408-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b408-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b408-105">DESCRIPTION</span></span>
<span data-ttu-id="6b408-106">Polecenie cmdlet **Invoke-AzSqlInstanceFailover failovers** an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="6b408-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6b408-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b408-107">EXAMPLES</span></span>

### <span data-ttu-id="6b408-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b408-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="6b408-109">To polecenie będzie trybu failover podstawowej repliki wystąpienia o nazwie "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="6b408-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="6b408-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6b408-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="6b408-111">To polecenie będzie trybu failover czytelnej repliki pomocniczej zarządzanego wystąpienia "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="6b408-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="6b408-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b408-112">PARAMETERS</span></span>

### <span data-ttu-id="6b408-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6b408-113">-AsJob</span></span>
<span data-ttu-id="6b408-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b408-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b408-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b408-115">-DefaultProfile</span></span>
<span data-ttu-id="6b408-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b408-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b408-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6b408-117">-Force</span></span>
<span data-ttu-id="6b408-118">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="6b408-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6b408-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6b408-119">-Name</span></span>
<span data-ttu-id="6b408-120">Nazwa wystąpienia języka Azure SQL do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6b408-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="6b408-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b408-121">-PassThru</span></span>
<span data-ttu-id="6b408-122">Po pomyślnym wykonaniu zwraca wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="6b408-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="6b408-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6b408-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b408-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6b408-124">-ReadableSecondary</span></span>
<span data-ttu-id="6b408-125">Failover the readable secondary replica instead of the default primary replica</span><span class="sxs-lookup"><span data-stu-id="6b408-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="6b408-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b408-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b408-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b408-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b408-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b408-128">-Confirm</span></span>
<span data-ttu-id="6b408-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6b408-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b408-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b408-130">-WhatIf</span></span>
<span data-ttu-id="6b408-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b408-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b408-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6b408-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b408-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b408-133">CommonParameters</span></span>
<span data-ttu-id="6b408-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b408-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b408-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b408-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b408-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b408-136">INPUTS</span></span>

### <span data-ttu-id="6b408-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b408-137">System.String</span></span>

## <span data-ttu-id="6b408-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b408-138">OUTPUTS</span></span>

## <span data-ttu-id="6b408-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b408-139">NOTES</span></span>

## <span data-ttu-id="6b408-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b408-140">RELATED LINKS</span></span>
