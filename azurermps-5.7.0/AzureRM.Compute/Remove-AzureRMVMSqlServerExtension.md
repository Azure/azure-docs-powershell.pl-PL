---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526945"
---
# <span data-ttu-id="50e66-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="50e66-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="50e66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50e66-102">SYNOPSIS</span></span>
<span data-ttu-id="50e66-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50e66-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50e66-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="50e66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50e66-105">DESCRIPTION</span></span>
<span data-ttu-id="50e66-106">Polecenie cmdlet **Remove-AzureRmVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50e66-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="50e66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50e66-107">EXAMPLES</span></span>

### <span data-ttu-id="50e66-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="50e66-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="50e66-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="50e66-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="50e66-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50e66-110">PARAMETERS</span></span>

### <span data-ttu-id="50e66-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50e66-111">-Name</span></span>
<span data-ttu-id="50e66-112">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50e66-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="50e66-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e66-113">-ResourceGroupName</span></span>
<span data-ttu-id="50e66-114">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="50e66-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="50e66-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="50e66-115">-VMName</span></span>
<span data-ttu-id="50e66-116">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50e66-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="50e66-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e66-117">CommonParameters</span></span>
<span data-ttu-id="50e66-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e66-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e66-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e66-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e66-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50e66-120">INPUTS</span></span>

### <span data-ttu-id="50e66-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="50e66-121">None</span></span>
<span data-ttu-id="50e66-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="50e66-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50e66-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50e66-123">OUTPUTS</span></span>

## <span data-ttu-id="50e66-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50e66-124">NOTES</span></span>

## <span data-ttu-id="50e66-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50e66-125">RELATED LINKS</span></span>

[<span data-ttu-id="50e66-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="50e66-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="50e66-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="50e66-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


