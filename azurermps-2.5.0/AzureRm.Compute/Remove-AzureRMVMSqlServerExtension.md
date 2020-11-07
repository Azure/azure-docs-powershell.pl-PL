---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898964"
---
# <span data-ttu-id="1020f-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1020f-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="1020f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1020f-102">SYNOPSIS</span></span>
<span data-ttu-id="1020f-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1020f-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1020f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1020f-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1020f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1020f-105">DESCRIPTION</span></span>
<span data-ttu-id="1020f-106">Polecenie cmdlet **Remove-AzureRmVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1020f-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="1020f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1020f-107">EXAMPLES</span></span>

### <span data-ttu-id="1020f-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="1020f-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="1020f-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="1020f-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="1020f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1020f-110">PARAMETERS</span></span>

### <span data-ttu-id="1020f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1020f-111">-DefaultProfile</span></span>
<span data-ttu-id="1020f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1020f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1020f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1020f-113">-Name</span></span>
<span data-ttu-id="1020f-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1020f-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1020f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1020f-115">-ResourceGroupName</span></span>
<span data-ttu-id="1020f-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1020f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1020f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="1020f-117">-VMName</span></span>
<span data-ttu-id="1020f-118">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1020f-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1020f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1020f-119">CommonParameters</span></span>
<span data-ttu-id="1020f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1020f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1020f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1020f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1020f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1020f-122">INPUTS</span></span>

### <span data-ttu-id="1020f-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1020f-123">None</span></span>
<span data-ttu-id="1020f-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1020f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1020f-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1020f-125">OUTPUTS</span></span>

### <span data-ttu-id="1020f-126">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1020f-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1020f-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1020f-127">NOTES</span></span>

## <span data-ttu-id="1020f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1020f-128">RELATED LINKS</span></span>

[<span data-ttu-id="1020f-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1020f-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="1020f-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1020f-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


